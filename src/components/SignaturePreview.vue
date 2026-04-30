<!-- © 2026 Iheb Zmerli. Template ID: {{ uniqueId }}. Unauthorized use prohibited. -->
<template>
  <div class="preview">
    <table
      role="presentation"
      cellpadding="0"
      cellspacing="0"
      border="0"
      style="
        border-collapse: collapse;
        width: 700px;
        max-width: 100%;
        font-family: Poppins, Arial, sans-serif;
        color: var(--brand-color);
        line-height: 1.2;
      "
    >
      <tbody>
        <tr>
          <!-- LEFT SIDE -->
          <td style="padding: 8px 10px; vertical-align: top; width: 260px">

            <!-- NAME -->
            <div style="
                font-family: 'Brittany Signature', cursive;
                font-weight: 400;
                font-size: 31px;
                color: #000;
                width: 216px;
                height: 65px;
              ">
              {{ name }}
            </div>

            <!-- JOB -->
            <div style="
                font-size: 13px;
                margin-top: -10px;
                color: #231F20;
                font-family: 'Poppins', light;
              ">
              {{ jobTitle }}
            </div>

            <!-- PHONES -->
            <table role="presentation" cellpadding="0" cellspacing="0" border="0" style="margin-top: 10px">
              <tbody>
                <tr>
                  <td style="width: 20px; vertical-align: middle">
                    <a :href="'tel:' + office" target="_blank" rel="noopener noreferrer"
                      style="text-decoration: none; display: inline-block">
                        <table role="presentation" cellpadding="0" cellspacing="0" border="0">
                        <tbody>
                          <tr>
                            <td align="center" valign="middle"
                                :style="{
                                  width: '20px',
                                  height: '20px',
                                  background: companyColor,
                                  borderRadius: '50%'
                                }">

                              <img
                                src="https://raw.githubusercontent.com/ihebZmez/signature-generator/main/public/images-template-icons/v2_10.png"
                                width="12"
                                height="12"
                                style="display:block; border:0;"
                              />

                            </td>
                          </tr>
                        </tbody>
                      </table>
                    </a>
                  </td>
                  <td style="padding-left: 10px; font-size: 12px; color: #231F20; font-family: 'Poppins', light;">
                    {{ office }}
                  </td>
                  <td style="padding: 0 10px; font-size: 12px; color: #231F20; font-family: 'Poppins', light;">
                    |
                  </td>
                  <td style="font-size: 12px; color: #231F20; font-family: 'Poppins', light;">
                    {{ mobile }}
                  </td>
                </tr>
              </tbody>
            </table>

            <!-- WEBSITE -->
            <table role="presentation" cellpadding="0" cellspacing="0" border="0" style="margin-top: 10px">
              <tbody>
                <tr>
                  <td style="width: 20px; vertical-align: middle">
                    <a :href="company.url" target="_blank" rel="noopener noreferrer"
                      style="text-decoration: none; display: inline-block">
                      <table role="presentation" cellpadding="0" cellspacing="0" border="0">
                        <tbody>
                          <tr>
                            <td align="center" valign="middle"
                                :style="{
                                  width: '20px',
                                  height: '20px',
                                  background: companyColor,
                                  borderRadius: '50%'
                                }">

                              <img
                                src="https://raw.githubusercontent.com/ihebZmez/signature-generator/main/public/images-template-icons/v2_11.png"
                                width="12"
                                height="12"
                                style="display:block; border:0;"
                              />

                            </td>
                          </tr>
                        </tbody>
                      </table>
                    </a>
                  </td>
                  <td style="padding-left: 10px; font-size: 12px; color: #231F20;">
                    {{ companyUrlReadable }}
                  </td>
                </tr>
              </tbody>
            </table>

            <!-- ADDRESS -->
            <table role="presentation" cellpadding="0" cellspacing="0" border="0" style="margin-top: 10px">
              <tbody>
                <tr>
                  <td style="width: 20px; vertical-align: top">
                    <a :href="'https://maps.google.com/?q=' + encodeURIComponent(companyAddress)" target="_blank" rel="noopener noreferrer"
                      style="text-decoration: none; display: inline-block">
                      <table role="presentation" cellpadding="0" cellspacing="0" border="0">
                        <tbody>
                          <tr>
                            <td align="center" valign="middle"
                                :style="{
                                  width: '20px',
                                  height: '20px',
                                  background: companyColor,
                                  borderRadius: '50%'
                                }">

                              <img
                                src="https://raw.githubusercontent.com/ihebZmez/signature-generator/main/public/images-template-icons/v2_12.png"
                                width="12"
                                height="12"
                                style="display:block; border:0;"
                              />

                            </td>
                          </tr>
                        </tbody>
                      </table>
                    </a>
                  </td>
                  <td style="padding-left: 10px; font-size: 12px; color: #231F20; font-family: 'Poppins', light;">
                    <span v-html="companyAddress"></span>
                  </td>
                </tr>
              </tbody>
            </table>

          </td>

          <!-- RIGHT SIDE -->
          <td style="vertical-align: top; width: 300px; text-align: center; padding: 7px 0;">

            <!-- LOGO -->
            <img
              :src="companyLogo"
              :alt="company.name"
              style="width: 200px; height: auto; border: 0; display: block; margin: 5px auto 0;"
            />

            <!-- SOCIAL -->
            <table role="presentation" cellpadding="0" cellspacing="0" border="0" align="center"
              style="margin-top: 8px; margin-left: auto">
              <tbody>
                <tr>
                  <td v-for="icon in socialIcons" :key="icon.link" style="padding-right: 9px">
                    <a :href="icon.link" target="_blank" rel="noopener noreferrer"
                      style="text-decoration: none; display: inline-block">
                      <span :style="socialStyle">
                        &#8203;
                        <img
                          :src="icon.img"
                          :alt="icon.alt"
                          style="position: absolute; top: 2px; left: 2px; width: 28px; height: 28px; border: 0;"
                        />
                      </span>
                    </a>
                  </td>
                </tr>
              </tbody>
            </table>

          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: "SignaturePreview",
  props: ["companies", "form"],

  computed: {
    company() {
      return this.companies.find(c => c.name === this.form.company) || {};
    },

    companyColor() {
      return this.company.color || "#ff3131";
    },

    iconStyle() {
      return {
        display: "inline-block",
        width: "16px",
        height: "16px",
        background: this.companyColor,
        borderRadius: "50%",
        position: "relative",
        WebkitUserSelect: "text",
        userSelect: "text",
      };
    },

    socialStyle() {
      return {
        display: "inline-block",
        width: "32px",
        height: "32px",
        background: this.companyColor,
        borderRadius: "50%",
        position: "relative",
        WebkitUserSelect: "text",
        userSelect: "text",
      };
    },

    companyLogo() {
      return this.company.logo;
    },

    companyUrlReadable() {
      return (this.company.url || "").replace(/(^\w+:|^)\/\//, "");
    },

    name() {
      return this.form.name?.trim() || "First Last";
    },

    jobTitle() {
      return this.form.jobTitle?.trim() || "Job Title";
    },

    office() {
      return this.form.office || "";
    },

    mobile() {
      return this.form.mobile || "";
    },

    companyAddress() {
      const value = this.form.companyAddress?.trim() || this.company.address || "";
      return value.replace(/\s{2,}/g, '<br>');
    },

    socialIcons() {
      const icons = [
        {
          link: this.company.socialIcons?.instagram || "#",
          img: "https://raw.githubusercontent.com/ihebZmez/signature-generator/main/public/images-template-icons/v1_4.png",
          alt: "Instagram"
        },
        {
          link: this.company.socialIcons?.fb || "#",
          img: "https://raw.githubusercontent.com/ihebZmez/signature-generator/main/public/images-template-icons/v1_5.png",
          alt: "Facebook"
        },
        {
          link: this.company.socialIcons?.tiktok || "#",
          img: "https://raw.githubusercontent.com/ihebZmez/signature-generator/main/public/images-template-icons/v1_6.png",
          alt: "TikTok"
        },
        {
          link: this.company.socialIcons?.linkedin || "#",
          img: "https://raw.githubusercontent.com/ihebZmez/signature-generator/main/public/images-template-icons/v1_7.png",
          alt: "LinkedIn"
        }
      ];

      // Filter out icons where link is "#", null, undefined, or empty string
      return icons.filter(icon => icon.link && icon.link.trim() !== "#" && icon.link.trim() !== "");
    }
  }
};
</script>

<style>
@import url('https://fonts.cdnfonts.com/css/brittany-signature');
@import url('https://fonts.cdnfonts.com/css/poppins');
</style>