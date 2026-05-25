<!-- © 2026 Iheb Zmerli. Template ID: {{ uniqueId }}. Unauthorized use prohibited. -->
<template>
  <div class="preview" :class="{ 'dark-mode': isDarkMode }">
    <!-- OUTER CADRE - Full signature wrapper -->
    <table
      role="presentation"
      cellpadding="0"
      cellspacing="0"
      border="0"
      width="670"
      style="
        border-collapse: collapse;
        width: 670px;
        max-width: 100%;
        font-family: Poppins, Arial, sans-serif;
        line-height: 1.2;
        border: 2px solid;
        border-radius: 16px;
        overflow: hidden;
      "
      :style="{ borderColor: companyColor }"
    >
      <tbody>
        <tr>
          <td style="padding: 20px">
            <!-- MAIN SIGNATURE TABLE with border -->
            <table
              role="presentation"
              cellpadding="0"
              cellspacing="0"
              border="0"
              width="670"
              style="
                border-collapse: collapse;
                width: 670px;
                max-width: 100%;
                font-family: Poppins, Arial, sans-serif;
                line-height: 1.2;
                border: 2px solid;
                border-radius: 16px;
                overflow: hidden;
                margin: 0 auto;
              "
              :style="{ borderColor: companyColor }"
            >
              <tbody>
                <tr>
                  <!-- LEFT SIDE - Solid brand color background -->
                  <td
                    style="
                      padding: 16px 12px;
                      vertical-align: top;
                      width: 450px;
                      background-color: #f5f5f5;
                      border-right: 2px dotted;
                    "
                    :style="{
                      backgroundColor: companyColor + '13',
                      borderRightColor: companyColor,
                    }"
                  >
                    <div style="padding: 5px 5px 5px 10px">
                      <!-- NAME -->
                      <div
                        class="signature-name"
                        style="
                          font-family: Georgia, serif;
                          font-weight: 500;
                          font-size: 32px;
                          color: #1a1a1a;
                          margin-bottom: 8px;
                          letter-spacing: -0.5px;
                          white-space: normal;
                          word-wrap: break-word;
                        "
                        :style="{ color: companyColor }"
                      >
                        {{ name }}
                      </div>

                      <!-- JOB with rounded pill background -->
                      <div
                        class="signature-job"
                        style="
                          font-size: 13px;
                          margin-bottom: 16px;
                          color: #555;
                          font-family: 'Poppins', Arial, sans-serif;
                          font-weight: 500;
                          background-color: rgba(0, 0, 0, 0.05);
                          display: inline-block;
                          padding: 5px 14px;
                          border-radius: 25px;
                          letter-spacing: 0.3px;
                        "
                      >
                        {{ jobTitle }}
                      </div>

                      <!-- DIVIDER -->
                      <div
                        style="
                          height: 1px;
                          background: linear-gradient(
                            90deg,
                            #ddd 0%,
                            transparent 100%
                          );
                          margin: 12px 0 14px 0;
                        "
                        :style="{
                          background:
                            'linear-gradient(90deg, ' +
                            companyColor +
                            '40 0%, transparent 100%)',
                        }"
                      ></div>

                      <!-- PHONES -->
                      <table
                        role="presentation"
                        cellpadding="0"
                        cellspacing="0"
                        border="0"
                        style="margin-bottom: 10px"
                      >
                        <tbody>
                          <tr>
                            <td style="width: 28px; vertical-align: middle">
                              <table
                                role="presentation"
                                cellpadding="0"
                                cellspacing="0"
                                border="0"
                              >
                                <tbody>
                                  <tr>
                                    <td
                                      align="center"
                                      valign="middle"
                                      style="
                                        width: 26px;
                                        height: 26px;
                                        background-color: #e8e8e8;
                                        border-radius: 50%;
                                      "
                                      :style="{ backgroundColor: companyColor }"
                                    >
                                      <img
                                        src="https://raw.githubusercontent.com/ihebZmez/signature-generator/main/public/images-template-icons/v2_10.png"
                                        width="13"
                                        height="13"
                                        style="
                                          display: block;
                                          border: 0;
                                          margin: 0 auto;
                                        "
                                      />
                                    </td>
                                  </tr>
                                </tbody>
                              </table>
                            </td>
                            <td
                              v-if="office"
                              style="
                                padding-left: 10px;
                                font-size: 12px;
                                color: #333;
                                font-family: 'Poppins', Arial, sans-serif;
                              "
                            >
                              {{ office }}
                            </td>
                            <td
                              v-if="office && mobile"
                              style="
                                padding: 0 8px;
                                font-size: 12px;
                                color: #999;
                              "
                            >
                              |
                            </td>
                            <td
                              v-if="mobile"
                              style="
                                font-size: 12px;
                                color: #333;
                                font-family: 'Poppins', Arial, sans-serif;
                              "
                            >
                              {{ mobile }}
                            </td>
                          </tr>
                        </tbody>
                      </table>

                      <!-- WEBSITE -->
                      <table
                        role="presentation"
                        cellpadding="0"
                        cellspacing="0"
                        border="0"
                        style="margin-bottom: 10px"
                      >
                        <tbody>
                          <tr>
                            <td style="width: 28px; vertical-align: middle">
                              <table
                                role="presentation"
                                cellpadding="0"
                                cellspacing="0"
                                border="0"
                              >
                                <tbody>
                                  <tr>
                                    <td
                                      align="center"
                                      valign="middle"
                                      style="
                                        width: 26px;
                                        height: 26px;
                                        background-color: #e8e8e8;
                                        border-radius: 50%;
                                      "
                                      :style="{ backgroundColor: companyColor }"
                                    >
                                      <img
                                        src="https://raw.githubusercontent.com/ihebZmez/signature-generator/main/public/images-template-icons/v2_11.png"
                                        width="13"
                                        height="13"
                                        style="
                                          display: block;
                                          border: 0;
                                          margin: 0 auto;
                                        "
                                      />
                                    </td>
                                  </tr>
                                </tbody>
                              </table>
                            </td>
                            <td
                              style="
                                padding-left: 10px;
                                font-size: 12px;
                                color: #333;
                                font-family: 'Poppins', Arial, sans-serif;
                              "
                            >
                              <a
                                :href="company.url"
                                target="_blank"
                                rel="noopener noreferrer"
                                style="color: #555; text-decoration: none"
                              >
                                {{ companyUrlReadable }}
                              </a>
                            </td>
                          </tr>
                        </tbody>
                      </table>

                      <!-- ADDRESS -->
                      <table
                        role="presentation"
                        cellpadding="0"
                        cellspacing="0"
                        border="0"
                      >
                        <tbody>
                          <tr>
                            <td style="width: 28px; vertical-align: top">
                              <table
                                role="presentation"
                                cellpadding="0"
                                cellspacing="0"
                                border="0"
                              >
                                <tbody>
                                  <tr>
                                    <td
                                      align="center"
                                      valign="middle"
                                      style="
                                        width: 26px;
                                        height: 26px;
                                        background-color: #e8e8e8;
                                        border-radius: 50%;
                                      "
                                      :style="{ backgroundColor: companyColor }"
                                    >
                                      <img
                                        src="https://raw.githubusercontent.com/ihebZmez/signature-generator/main/public/images-template-icons/v2_13.png"
                                        width="13"
                                        height="13"
                                        style="
                                          display: block;
                                          border: 0;
                                          margin: 0 auto;
                                        "
                                      />
                                    </td>
                                  </tr>
                                </tbody>
                              </table>
                            </td>
                            <td
                              style="
                                padding-left: 10px;
                                font-size: 12px;
                                color: #555;
                                font-family: 'Poppins', Arial, sans-serif;
                                line-height: 1.4;
                              "
                            >
                              <span v-html="companyAddress"></span>
                            </td>
                          </tr>
                        </tbody>
                      </table>
                    </div>
                  </td>

                  <!-- RIGHT SIDE - Subtle gray background (survives dark mode) -->
                  <td
                    style="
                      vertical-align: top;
                      width: 260px;
                      text-align: center;
                      padding: 10px 12px 16px 12px;
                      background-color: #fafafa;
                    "
                    :style="{ backgroundColor: companyColor + '30' }"
                  >
                    <!-- CENTERED CONTAINER for logo + social icons -->
                    <div style="display: inline-block; text-align: center;">
                      <!-- LOGO -->
                      <img
                        :src="companyLogo"
                        :alt="company.name"
                        :style="logoStyle"
                        style="max-width: 100%; height: auto; display: block; margin: 0 auto;"
                      />

                      <!-- DIVIDER -->
                      <div
                        style="
                          height: 1px;
                          background: #e0e0e0;
                          margin: 15px 0px;
                        "
                        :style="{ background: companyColor + '30' }"
                      ></div>

                      <!-- SOCIAL ICONS -->
                      <table
                        role="presentation"
                        cellpadding="0"
                        cellspacing="0"
                        border="0"
                        align="center"
                        :style="{ margin: socialIconsMarginBg || '20px 0px 40px 0px' }"
                      >
                        <tbody>
                          <tr>
                            <td
                              v-for="(icon, index) in socialIcons"
                              :key="icon.link"
                              :style="{
                                paddingRight:
                                  index === socialIcons.length - 1
                                    ? '0px'
                                    : '10px',
                                verticalAlign: 'middle',
                              }"
                            >
                              <a
                                :href="icon.link"
                                target="_blank"
                                rel="noopener noreferrer"
                                style="
                                  text-decoration: none;
                                  display: inline-block;
                                "
                              >
                                <table
                                  role="presentation"
                                  cellpadding="0"
                                  cellspacing="0"
                                  border="0"
                                >
                                  <tbody>
                                    <tr>
                                      <td
                                        align="center"
                                        valign="middle"
                                        style="
                                          width: 34px;
                                          height: 34px;
                                          background-color: #e8e8e8;
                                          border-radius: 50%;
                                          transition: all 0.2s ease;
                                        "
                                        :style="{ backgroundColor: companyColor }"
                                      >
                                        <img
                                          :src="icon.img"
                                          :alt="icon.alt"
                                          width="20"
                                          height="20"
                                          style="
                                            display: block;
                                            border: 0;
                                            margin: 0 auto;
                                          "
                                        />
                                      </td>
                                    </tr>
                                  </tbody>
                                </table>
                              </a>
                            </td>
                          </tr>
                        </tbody>
                      </table>
                    </div>

                    <!-- POWERED BY LOGO -->
                    <img
                      v-if="form.showPoweredBy"
                      src="https://raw.githubusercontent.com/ihebZmez/signature-generator/main/public/logo/v1_2_poweredByCfac.png"
                      style="
                        width: 190px;
                        height: auto;
                        border: 0;
                        display: block;
                        margin: 15px auto 5px auto;
                        opacity: 0.7;
                      "
                    />
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
  props: ["companies", "form", "isDarkMode"],

  computed: {
    company() {
      return this.companies.find((c) => c.name === this.form.company) || {};
    },

    companyColor() {
      return this.company.color || "#6f4e37";
    },

    companyLogo() {
      return this.company.logo;
    },

    logoStyle() {
      const width = this.company.logoWidthBg || 210;
      const height = this.company.logoHeightBg || "auto";
      const margin = this.company.logoMarginBg || "0 auto 10px auto";

      const style = {
        border: "0",
        display: "block",
        margin: margin,
      };

      if (typeof width === "number" || !isNaN(parseFloat(width))) {
        style.width = typeof width === "number" ? width + "px" : width;
      } else {
        style.width = width;
      }

      if (height && height !== "auto") {
        if (typeof height === "number" || !isNaN(parseFloat(height))) {
          style.height = typeof height === "number" ? height + "px" : height;
        } else {
          style.height = height;
        }
      } else {
        style.height = "auto";
      }

      return style;
    },

    socialIconsMarginBg() {
      return this.company.socialIconsMarginBg || "20px 0px 40px 0px";
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
      const value =
        this.form.companyAddress?.trim() || this.company.address || "";
      return value.replace(/\s{2,}/g, "<br>");
    },

    socialIcons() {
      const icons = [
        {
          link: this.company.socialIcons?.instagram || "#",
          img: "https://raw.githubusercontent.com/ihebZmez/signature-generator/main/public/images-template-icons/v1_4.png",
          alt: "Instagram",
        },
        {
          link: this.company.socialIcons?.fb || "#",
          img: "https://raw.githubusercontent.com/ihebZmez/signature-generator/main/public/images-template-icons/v1_5.png",
          alt: "Facebook",
        },
        {
          link: this.company.socialIcons?.tiktok || "#",
          img: "https://raw.githubusercontent.com/ihebZmez/signature-generator/main/public/images-template-icons/v1_6.png",
          alt: "TikTok",
        },
        {
          link: this.company.socialIcons?.linkedin || "#",
          img: "https://raw.githubusercontent.com/ihebZmez/signature-generator/main/public/images-template-icons/v1_7.png",
          alt: "LinkedIn",
        },
      ];

      return icons.filter(
        (icon) =>
          icon.link && icon.link.trim() !== "#" && icon.link.trim() !== "",
      );
    },
  },
};
</script>

<style>
@import url("https://fonts.cdnfonts.com/css/poppins");
@import url("https://fonts.cdnfonts.com/css/georgia");

/* ─── MANUAL DARK MODE TOGGLE ─── */
.preview.dark-mode .signature-name,
.preview.dark-mode .signature-job,
.preview.dark-mode td:not([style*="border-radius: 50%"]),
.preview.dark-mode span:not([style*="border-radius: 50%"]),
.preview.dark-mode a {
  color: #ffffff !important;
}

.preview.dark-mode td[style*="background-color: #f5f5f5"],
.preview.dark-mode td[style*="background-color: #fafafa"] {
  background-color: #2a2a2a !important;
}

/* DO NOTHING to circular icons - keep them exactly as they are */
/* No styles for td[style*="border-radius: 50%"] in dark mode */

/* ─── GMAIL DARK MODE ─── */
@media (prefers-color-scheme: dark) {
  td[style*="background-color: #f5f5f5"],
  td[style*="background-color: #fafafa"] {
    background-color: #2a2a2a !important;
    -webkit-print-color-adjust: exact;
    print-color-adjust: exact;
  }

  .signature-name,
  .signature-job,
  td[style*="color: #333"],
  td[style*="color: #555"],
  td[style*="color: #1a1a1a"] {
    color: #ffffff !important;
  }

  /* DO NOTHING to circular icons in Gmail dark mode either */
  /* No styles for td[style*="border-radius: 50%"] here */

  img {
    filter: none !important;
  }
}

/* ─── MOBILE ─── */
/* Fix for long names on mobile */
@media screen and (max-width: 480px) {
  table[width="670"] {
    width: 100% !important;
  }

  td[style*="width: 450px"] {
    width: 60% !important;
    display: block !important;
    width: 100% !important;
  }

  td[style*="width: 260px"] {
    width: 100% !important;
    display: block !important;
  }

  .signature-name {
    font-size: 20px !important;
    white-space: normal !important;
    word-wrap: break-word !important;
    line-height: 1.2 !important;
    margin-bottom: 8px !important;
  }

  /* Make left side stack on top on mobile */
  .preview table tbody tr {
    display: flex;
    flex-direction: column;
  }

  .preview table tbody tr td:first-child {
    border-right: none !important;
    border-bottom: 2px dotted;
    border-bottom-color: v-bind(companyColor);
    border-radius: 16px 16px 0 0 !important;
  }

  .preview table tbody tr td:last-child {
    border-radius: 0 0 16px 16px !important;
  }

  /* Adjust social icons on mobile */
  .preview td[style*="margin: 20px 0px 40px 70px"] {
    margin: 15px auto !important;
    text-align: center !important;
  }
}
</style>
