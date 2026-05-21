<!-- © 2026 Iheb Zmerli. Template ID: {{ uniqueId }}. Unauthorized use prohibited. -->
<template>
  <div class="preview" :class="{ 'dark-mode': isDarkMode }" style="padding: 20px; border-radius: 8px; background-color: #ffffff;">
    <table
      role="presentation"
      cellpadding="0"
      cellspacing="0"
      border="0"
      style="
        border-collapse: collapse;
        width: 670px;
        height: 170px;
        max-width: 100%;
        font-family: Poppins, Arial, sans-serif;
        color: var(--brand-color);
        line-height: 1.2;
      "
    >
      <tbody>
        <tr>
          <!-- LEFT SIDE -->
          <td style="padding: 8px 10px; vertical-align: top; width: auto; min-width: 340px;">

            <!-- NAME -->
            <div class="signature-name" style="
                font-family: Georgia, sans-serif;
                font-weight: 400;
                font-size: 30px;
                color: #000;
                max-width: none;
                width: auto;
                white-space: nowrap;
                margin-bottom: 12px;
              ">
                {{ name }}
            </div>

            <!-- JOB -->
            <div class="signature-job" style="
                font-size: 13px;
                margin-bottom: 12px;
                color: #231F20;
                font-family: 'Poppins', light;
              ">
              {{ jobTitle }}
            </div>

            <!-- PHONES -->
            <table role="presentation" cellpadding="0" cellspacing="0" border="0" style="margin-top: 12px">
              <tbody>
                <tr>
                  <td style="width: 17px; vertical-align: middle">
                    <a :href="'tel:' + office" target="_blank" rel="noopener noreferrer"
                      style="text-decoration: none; display: inline-block">
                        <table role="presentation" cellpadding="0" cellspacing="0" border="0">
                        <tbody>
                          <tr>
                            <td align="center" valign="middle"
                                :style="{
                                  width: '17px',
                                  height: '17px',
                                  background: companyColor,
                                  borderRadius: '50%'
                                }">

                              <img
                                src="https://raw.githubusercontent.com/ihebZmez/signature-generator/main/public/images-template-icons/v2_10.png"
                                width="11"
                                height="11"
                                style="display:block; border:0;"
                              />

                            </td>
                          </tr>
                        </tbody>
                      </table>
                    </a>
                  </td>
                  <td v-if="office" style="padding-left: 8px; font-size: 12px; color: #231F20; font-family: 'Poppins', light; white-space: nowrap;">
                    {{ office }}
                  </td>
                  <td v-if="office && mobile" style="padding: 0 8px; font-size: 12px; color: #231F20; font-family: 'Poppins', light;">
                    |
                  </td>
                  <td v-if="mobile" style="font-size: 12px; color: #231F20; font-family: 'Poppins', light; white-space: nowrap;">
                    {{ mobile }}
                  </td>
                </tr>
              </tbody>
            </table>

            <!-- WEBSITE -->
            <table role="presentation" cellpadding="0" cellspacing="0" border="0" style="margin-top: 12px">
              <tbody>
                <tr>
                  <td style="width: 17px; vertical-align: middle">
                    <a :href="company.url" target="_blank" rel="noopener noreferrer"
                      style="text-decoration: none; display: inline-block">
                      <table role="presentation" cellpadding="0" cellspacing="0" border="0">
                        <tbody>
                          <tr>
                            <td align="center" valign="middle"
                                :style="{
                                  width: '17px',
                                  height: '17px',
                                  background: companyColor,
                                  borderRadius: '50%'
                                }">

                              <img
                                src="https://raw.githubusercontent.com/ihebZmez/signature-generator/main/public/images-template-icons/v2_11.png"
                                width="11"
                                height="11"
                                style="display:block; border:0;"
                              />

                            </td>
                          </tr>
                        </tbody>
                      </table>
                    </a>
                  </td>
                  <td style="padding-left: 8px; font-size: 12px; color: #231F20;">
                    {{ companyUrlReadable }}
                  </td>
                </tr>
              </tbody>
            </table>

            <!-- ADDRESS -->
            <table role="presentation" cellpadding="0" cellspacing="0" border="0" style="margin-top: 12px">
              <tbody>
                <tr>
                  <td style="width: 17px; vertical-align: top">
                    <a :href="'https://maps.google.com/?q=' + encodeURIComponent(companyAddress)" target="_blank" rel="noopener noreferrer"
                      style="text-decoration: none; display: inline-block">
                      <table role="presentation" cellpadding="0" cellspacing="0" border="0">
                        <tbody>
                          <tr>
                            <td align="center" valign="middle"
                                :style="{
                                  width: '17px',
                                  height: '17px',
                                  background: companyColor,
                                  borderRadius: '50%'
                                }">

                              <img
                                src="https://raw.githubusercontent.com/ihebZmez/signature-generator/main/public/images-template-icons/v2_13.png"
                                width="11"
                                height="11"
                                style="display:block; border:0;"
                              />
                            </td>
                          </tr>
                        </tbody>
                      </table>
                    </a>
                  </td>
                  <td style="padding-left: 8px; font-size: 12px; color: #231F20; font-family: 'Poppins', light;">
                    <span v-html="companyAddress"></span>
                  </td>
                </tr>
              </tbody>
            </table>

          </td>

          <!-- RIGHT SIDE -->
          <td style="vertical-align: top; width: 260px; text-align: center; padding: 12px 0;">

            <!-- LOGO -->
            <img
              :src="companyLogo"
              :alt="company.name"
              :style="logoStyle"
            />

            <!-- SOCIAL -->
            <table role="presentation" cellpadding="0" cellspacing="0" border="0" align="center">
              <tbody>
                <tr>
                  <td v-for="(icon, index) in socialIcons" :key="icon.link" 
                      :style="{ 
                        paddingRight: (index === socialIcons.length - 1) ? '0px' : '9px',
                        verticalAlign: 'middle' 
                      }">
                    <a :href="icon.link" target="_blank" rel="noopener noreferrer"
                      style="text-decoration: none; display: inline-block; line-height: 0;">
                      <span :style="socialStyle" style="display: inline-block; position: relative; width: 35px; height: 35px;">
                        <img
                          :src="icon.img"
                          :alt="icon.alt"
                          style="position: absolute; top: 2px; left: 2px; width: 30px; height: 30px; border: 0; margin-top: 2px; margin-left: 1px"
                        />
                      </span>
                    </a>
                  </td>
                </tr>
              </tbody>
            </table>

            <!-- LOGO -->
            <img
              src="https://raw.githubusercontent.com/ihebZmez/signature-generator/main/public/logo/v1_2_poweredByCfac.png"
              style="width: 195px; height: auto; border: 0; display: block; margin: 15px 52px 7px 60px;"
            />
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: "SignaturePreview",
  props: ["companies", "form", "isDarkMode"],

  computed: {
    company() {
      return this.companies.find(c => c.name === this.form.company) || {};
    },

    companyColor() {
      return this.company.color || "#ff3131";
    },

    socialStyle() {
      return {
        display: "inline-block",
        width: "30px",
        height: "30px",
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

    logoStyle() {
      // Get dimensions from company config or use defaults
      const width = this.company.logoWidth || 210;
      const height = this.company.logoHeight || 'auto';
      const margin = this.company.logoMargin || '4px 52px 7px 52px';
      
      // Build style object
      const style = {
        border: '0',
        display: 'block',
        margin: margin
      };
      
      // Apply width
      if (typeof width === 'number' || !isNaN(parseFloat(width))) {
        style.width = typeof width === 'number' ? width + 'px' : width;
      } else {
        style.width = width;
      }
      
      // Apply height (if specified and not 'auto')
      if (height && height !== 'auto') {
        if (typeof height === 'number' || !isNaN(parseFloat(height))) {
          style.height = typeof height === 'number' ? height + 'px' : height;
        } else {
          style.height = height;
        }
      } else {
        style.height = 'auto';
      }
      
      return style;
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
@import url('https://fonts.cdnfonts.com/css/georgia');

/* ─── MANUAL DARK MODE TOGGLE (Preview Only) ─── */
.preview.dark-mode {
  background-color: #1a1a1a !important;
  padding: 20px;
  border-radius: 8px;
}

.preview.dark-mode,
.preview.dark-mode div,
.preview.dark-mode td,
.preview.dark-mode span,
.preview.dark-mode font,
.preview.dark-mode a {
  color: #ffffff !important;
}

/* Icon circles → white in manual dark mode */
.preview.dark-mode td[style*="border-radius: 50%"],
.preview.dark-mode span[style*="border-radius: 50%"] {
  background: companyColor !important;
}

/* Icon images → dark (visible on white circles) */
.preview.dark-mode td[style*="border-radius: 50%"] img,
.preview.dark-mode span[style*="border-radius: 50%"] img {
  filter: brightness(0) !important;
}

/* ─── MOBILE RESPONSIVENESS ─── */
@media screen and (max-width: 480px) {
  table[style*="width: 620px"] {
    width: 100% !important;
  }

  td[style*="width: 340px"] {
    width: 60% !important;
    padding: 6px 8px !important;
  }

  td[style*="width: 260px"] {
    width: 40% !important;
    padding: 6px 0 !important;
  }

  .signature-name {
    font-size: 22px !important;
    height: auto !important;
    line-height: 1.1 !important;
  }

  .signature-job {
    font-size: 11px !important;
    margin-top: 2px !important;
  }

  img[style*="width: 140px"] {
    width: 100px !important;
  }

  td[style*="white-space: nowrap"] {
    font-size: 10px !important;
  }
}

/* ─── GMAIL DARK MODE SUPPORT (WebKit based) ─── */
/* This matches exactly how Gmail renders dark mode - using WebKit's color-scheme */
@media (prefers-color-scheme: dark) {
  /* Gmail's dark mode automatically inverts colors, but we need to preserve our circles */
  .preview {
    color-scheme: dark;
  }
  
  /* Preserve circular backgrounds - Gmail tries to invert them, force white */
  td[style*="border-radius: 50%"],
  span[style*="border-radius: 50%"],
  td[style*="background:"] td[style*="border-radius: 50%"] {
    background: #ffffff !important;
    -webkit-print-color-adjust: exact;
    print-color-adjust: exact;
    color-adjust: exact;
  }
  
  /* Make icon images dark/black on the white circles */
  td[style*="border-radius: 50%"] img,
  span[style*="border-radius: 50%"] img,
  td[style*="background:"] td[style*="border-radius: 50%"] img {
    filter: brightness(0) !important;
    -webkit-filter: brightness(0) !important;
  }
  
  /* Preserve original logo colors - Gmail dark mode tries to invert logos */
  img[style*="width: 210px"],
  img[style*="width: 195px"] {
    filter: none !important;
    -webkit-filter: none !important;
  }
  
  /* Keep company logos visible - prevent Gmail's dark mode from breaking them */
  img[src*="companyLogo"] {
    filter: none !important;
    -webkit-filter: none !important;
  }
}
</style>