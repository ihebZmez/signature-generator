<template>
  <div class="app">
    <header class="header">
      <div class="container">
        <div class="inner">
          <img src="@/assets/logo.png" alt="Logo" class="logo" />
          <h1>Signature Generator - CFAC GROUP</h1>
        </div>
      </div>
    </header>
    <main class="main">
      <div class="container">
        <div class="inner">
          <div class="form-section">
            <h2>Entrez les informations</h2>
            <div class="box">
              <SignatureForm
                :companies="companies"
                :form="form"
                :useCache="useCache"
                :isDarkMode="isDarkMode"
                @toggle-dark-mode="isDarkMode = !isDarkMode"
              />
              <SignatureIntegrations />
            </div>
          </div>
          <div class="preview-section">
            <div class="preview-sticky">
              <h2>Signature Preview</h2>
              <!-- Add :key to force re-render when component type changes -->
              <component
                :is="currentPreviewComponent"
                :key="currentPreviewComponent"
                :companies="companies"
                :form="form"
                ref="preview"
                class="box"
                :isDarkMode="isDarkMode"
              />
            </div>
          </div>
        </div>
      </div>
    </main>
  </div>
</template>

<script>
import SignatureForm from "./components/SignatureForm.vue";
import SignaturePreview from "./components/SignaturePreview.vue";
import SignaturePreviewBackground from "./components/SignaturePreview-background.vue";
import SignatureIntegrations from "./components/SignatureIntegrations.vue";

export default {
  name: "App",
  components: {
    SignatureForm,
    SignaturePreview,
    SignaturePreviewBackground,
    SignatureIntegrations,
  },
  data() {
    return {
      useCache: window.esgConfig.useCache || true,
      companies: window.esgConfig.companies || [],
      form: {
        company: "Company Name",
        name: "Name Surname",
        jobTitle: "Job Title",
        office: "+216 00 000 000",
        mobile: "+216 00 000 000",
        address: "Immeuble Narimane, Rue Chott Mariem, Montplaisir, 1073,Tunis, Tunisie",
        useWhiteBackground: false, // Add this default
        showPoweredBy: true, // Add this default if missing
      },
      isDarkMode: false,
    };
  },
  computed: {
    currentPreviewComponent() {
      // Return SignaturePreview-background if useWhiteBackground is true
      // Otherwise return the standard SignaturePreview
      return this.form.useWhiteBackground ? 'SignaturePreviewBackground' : 'SignaturePreview';
    }
  },
  watch: {
    // Optional: Watch for changes and log them
    'form.useWhiteBackground'(newVal) {
      console.log('Switching to:', newVal ? 'White Background' : 'Standard');
    }
  }
};
</script>