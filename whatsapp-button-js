function whatsappButton({
                            brandName = '',
                            buttonName = '',
                            brandSubtitleText = '',
                            welcomeMessage = '',
                            phoneNumber = '',
                            brandImageUrl = '',
                            callToAction = '',
                            buttonSize = 'large',
                            buttonMargin = 'false',
                            buttonIconSize = 22,
                        }) {
    let returnVal = `
      <div>
       <style>
         @font-face {
          font-family: 'Inter';
          font-style: normal;
          font-weight: 400;
          font-display: swap;
          src: url(https://fonts.gstatic.com/s/inter/v12/UcC73FwrK3iLTeHuS_fvQtMwCp50KnMa25L7W0Q5n-wU.woff2) format('woff2');
          unicode-range: U+0100-024F, U+0259, U+1E00-1EFF, U+2020, U+20A0-20AB, U+20AD-20CF, U+2113, U+2C60-2C7F, U+A720-A7FF;
        }

        @font-face {
          font-family: 'Inter';
          font-style: normal;
          font-weight: 400;
          font-display: swap;
          src: url(https://fonts.gstatic.com/s/inter/v12/UcC73FwrK3iLTeHuS_fvQtMwCp50KnMa1ZL7W0Q5nw.woff2) format('woff2');
          unicode-range: U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA, U+02DC, U+2000-206F, U+2074, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD;
        }

        @font-face {
          font-family: 'Inter';
          font-style: normal;
          font-weight: 700;
          font-display: swap;
          src: url(https://fonts.gstatic.com/s/inter/v12/UcC73FwrK3iLTeHuS_fvQtMwCp50KnMa25L7W0Q5n-wU.woff2) format('woff2');
          unicode-range: U+0100-024F, U+0259, U+1E00-1EFF, U+2020, U+20A0-20AB, U+20AD-20CF, U+2113, U+2C60-2C7F, U+A720-A7FF;
        }

        @font-face {
          font-family: 'Inter';
          font-style: normal;
          font-weight: 700;
          font-display: swap;
          src: url(https://fonts.gstatic.com/s/inter/v12/UcC73FwrK3iLTeHuS_fvQtMwCp50KnMa1ZL7W0Q5nw.woff2) format('woff2');
          unicode-range: U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA, U+02DC, U+2000-206F, U+2074, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD;
        }

          @font-face {
            font-family: 'Helvetica';
            font-style: normal;
            font-weight: normal;
            font-display: optional;
            src: local('Helvetica');
        }

         :root {
            --color-primary-900: hsl(230, 54%, 11%);
            --color-gray-700: hsl(240, 1%, 31%);
            --color-text-secondary: var(--color-gray-700);
            --color-whatsapp-green-light:hsl(142, 70%,49%);
            --color-whatsapp-green-dark:hsl(173, 86%, 20%)
        }

        .font-header {
            font-family: "Inter", "Noto Sans TC", "Noto Sans SC", "Helvetica", "Arial", sans-serif;
            font-weight: 700 !important;
        }
      *,
*:before,
*:after {
    box-sizing: border-box;
}

.wa-widget-wrapper {
    position:fixed;
    right:40px;
    bottom:40px;
    display: flex;
    max-width: 498px;
    width:calc(100vw - 80px);
    flex-direction: column;
    z-index: 9999;
}

.wa-widget-brand-image {
    width:48px;
    height: 48px;
    border-radius: 500px;
}

.wa-widget-body {
    font-family: "Inter", "Noto Sans TC", "Noto Sans SC", "Helvetica", "Arial", sans-serif;
    margin-bottom: 16px;
    display: grid;
    height:453px;
    width:100%;
    grid-template-rows: 81px minmax(0px, 1fr) 124px;
    overflow: hidden;
    border-radius: 24px;
    background-color: white;
    box-shadow: 0px 24px 50px 10px rgba(0, 102, 255, 0.07);
}

.wa-widget-body-inner {
    padding: 16px 24px;
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    background-color: var(--color-whatsapp-green-dark);
}

.wa-chat-wrapper {
    position: relative;
    display: flex;
    height: 100%;
    width: 100%;
    background-color: white;
    padding: 24px;
}

.wa-chat-bubble-wrapper {
    z-index: 10;
    display: flex;
    height: max-content;
    max-height: 100%;
    width: auto;
    flex-direction: column;
    overflow: auto;
    border-radius: 16px;
    background-color: white;
    padding:24px;
}

.start-chat-section {
    z-index: 50;
    display: flex;
    width:100%;
    background-color: white;
    padding: 20px 24px;

    flex-direction: column;
}

.start-chat-button:hover {
    opacity: 80%;
    transition: 0.3s;
}

.start-chat-button {
    cursor: pointer;
    justify-content: center;
    border-width:0;
    display: flex;
    height: 56px;
    width: 100%;
    align-items: center;
    align-self: end;
    border-radius: 500px;
    background-color: var(--color-whatsapp-green-light);
}

.start-chat-button-inner {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
}
.start-chat-label {
    color: white;
    font-size: 1rem;
    padding-left: 8px;
}

.wa-cta-button:hover {
    opacity: 80%;
    transition: 0.3s;
}

.wa-cta-button {
    cursor: pointer;
    justify-content: center;
    border-width:0;
    display: flex;
    width: auto;
    align-items: center;
    align-self: end;
    border-radius: 500px;
    background-color: var(--color-whatsapp-green-light);
}

.wa-button-size-regular {
    padding:9px;
}

.wa-button-size-medium {
    padding:13px;
}

.wa-button-size-large {
    padding: 17px;
}

.wa-button-size-with-words {
    padding-right: 40px !important;
    padding-left:40px !important;
}

.wa-cta-button-inner {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
}

#wa-close-btn {
    cursor: pointer;
}

.wa-cta-button-label-margin {
    margin-left: 8px;
}

.wa-cta-button-label {
    color: white;
    font-size: 1rem;
    margin-top:0;
    margin-bottom: 0;
}

.wa-sleekflow-label {
    color:hsl(209 77% 60%);
    text-decoration: none;
}

.wa-powered-by-label {
    margin-top:12px;
    text-align:center;
}
      </style>

<div class="wa-widget-wrapper">
   <div id="wa-chat-window" class="wa-widget-body">
      <div class="wa-widget-body-inner">
         <div style="display:flex;width:100%">
            <img src="{{brandImageUrl}}" class="wa-widget-brand-image"/>
            <div style="padding-left:8px;display:flex;flex-direction:column;color:white">
               <p class="font-header" style="font-size:1.25rem;font-weight:500;line-height:1.5rem;margin:0">
                  {{brandName}}
               </p>
               <p style="margin:0;font-size:0.875rem;line-height:1.25rem">{{brandSubtitleText}}</p>
            </div>
         </div>
         <svg viewBox="0 0 15 14" fill="#000" xmlns="http://www.w3.org/2000/svg" id="wa-close-btn" width="20"
            height="20" style="background-color:transparent;fill:white;color:white">
            <path
               d="m2.674.569.106.093 4.754 4.754L12.288.662a1.12 1.12 0 0 1 1.678 1.48l-.094.105L9.118 7l4.754 4.753a1.12 1.12 0 0 1-1.479 1.678l-.105-.093-4.754-4.754-4.754 4.754a1.12 1.12 0 0 1-1.678-1.479l.093-.105L5.95 7 1.195 2.247A1.12 1.12 0 0 1 2.675.569Z">
            </path>
         </svg>
      </div>
      <div class="wa-chat-wrapper">
         <div class="wa-chat-bubble-wrapper">
            <p
               style="font-weight:500;font-family:Matter;margin-bottom:8px;margin-top:0px;color:var(--color-primary-900)">
               {{brandName}}
            </p>
            <p style="color:var(--color-gray-700);margin:0px">{{welcomeMessage}}</p>
         </div>
         <img style="max-width:100%;top:0;left:0;position:absolute;object-fit:cover" alt="WhatsApp Background" src="https://sleekflow-website-kvhdjfcmb-sleekflow.vercel.app/static/images/whatsapp-button-generator/whatsApp-bg.jpeg"/>
      </div>
      <div class="start-chat-section">
         <a rel="noopener noreferrer" target="_blank"
            style="text-decoration:none;width:100%"
            href="https://api.whatsapp.com/send?phone={{phoneNumber}}&amp;text={{welcomeMessage}}">
            <button class="start-chat-button">
               <div class="start-chat-button-inner">
                  <svg viewBox="0 0 22 22" fill="none" xmlns="http://www.w3.org/2000/svg" width="22" height="22">
                     <path d="m.76 21.24 1.412-5.12A10.324 10.324 0 0 1 .76 10.93C.76 5.35 5.35.76 10.964.76 16.58.76 21.24 5.35 21.24 10.93c0 5.578-4.661 10.31-10.276 10.31-1.765 0-3.46-.565-4.978-1.413L.76 21.24Z" fill="#EDEDED"></path>
                     <path d="m6.268 17.991.318.177c1.307.812 2.825 1.306 4.414 1.306 4.626 0 8.474-3.848 8.474-8.545 0-4.696-3.848-8.404-8.51-8.404-4.66 0-8.439 3.743-8.439 8.404 0 1.624.46 3.213 1.307 4.555l.212.318-.812 2.966 3.036-.777Z" fill="#25D366"></path>
                     <path d="m8.245 6.198-.671-.036a.802.802 0 0 0-.565.212c-.318.283-.848.812-.989 1.519-.247 1.059.141 2.33 1.06 3.601.918 1.271 2.683 3.32 5.79 4.202.989.283 1.766.106 2.402-.282.494-.318.812-.812.918-1.342l.105-.494a.355.355 0 0 0-.176-.389l-2.225-1.024a.337.337 0 0 0-.423.106l-.883 1.13a.275.275 0 0 1-.283.07c-.6-.211-2.613-1.059-3.707-3.177-.036-.106-.036-.212.035-.283l.848-.953c.07-.106.105-.247.07-.353L8.527 6.41a.308.308 0 0 0-.282-.212Z" fill="#FEFEFE"></path>
                  </svg>
                  <p class="start-chat-label font-header">{{callToAction}}</p>
               </div>
            </button>
         </a>
          <p class="wa-powered-by-label">
          <a rel="noopener noreferrer" target="_blank" class="wa-sleekflow-label" href="https://www.yamanhacioglu.com">
            <span>Northlab</span>
          </a>
          ⚡ Tarafından Desteklenmektedir!
        </p>
      </div>
   </div>
   <button id="wa-cta-button" class="wa-cta-button wa-button-size-{{buttonSize}} {{buttonPadding}}">
      <div class="wa-cta-button-inner">
         <svg viewBox="0 0 22 22" fill="none" xmlns="http://www.w3.org/2000/svg" width="{{buttonIconSize}}" height="{{buttonIconSize}}">
            <path d="m.76 21.24 1.412-5.12A10.324 10.324 0 0 1 .76 10.93C.76 5.35 5.35.76 10.964.76 16.58.76 21.24 5.35 21.24 10.93c0 5.578-4.661 10.31-10.276 10.31-1.765 0-3.46-.565-4.978-1.413L.76 21.24Z" fill="#EDEDED"></path>
            <path d="m6.268 17.991.318.177c1.307.812 2.825 1.306 4.414 1.306 4.626 0 8.474-3.848 8.474-8.545 0-4.696-3.848-8.404-8.51-8.404-4.66 0-8.439 3.743-8.439 8.404 0 1.624.46 3.213 1.307 4.555l.212.318-.812 2.966 3.036-.777Z" fill="#25D366"></path>
            <path d="m8.245 6.198-.671-.036a.802.802 0 0 0-.565.212c-.318.283-.848.812-.989 1.519-.247 1.059.141 2.33 1.06 3.601.918 1.271 2.683 3.32 5.79 4.202.989.283 1.766.106 2.402-.282.494-.318.812-.812.918-1.342l.105-.494a.355.355 0 0 0-.176-.389l-2.225-1.024a.337.337 0 0 0-.423.106l-.883 1.13a.275.275 0 0 1-.283.07c-.6-.211-2.613-1.059-3.707-3.177-.036-.106-.036-.212.035-.283l.848-.953c.07-.106.105-.247.07-.353L8.527 6.41a.308.308 0 0 0-.282-.212Z" fill="#FEFEFE"></path>
         </svg>
         <p class="wa-cta-button-label font-header {{buttonMargin}}">{{buttonName}}</p>
      </div>
   </button>
</div>

        </div>
       `;
    // Replace templated strings
    returnVal = returnVal.replaceAll('{{buttonName}}', buttonName);
    returnVal = returnVal.replaceAll('{{brandImageUrl}}', brandImageUrl);
    returnVal = returnVal.replaceAll('{{brandName}}', brandName);
    returnVal = returnVal.replaceAll('{{brandSubtitleText}}', brandSubtitleText);
    returnVal = returnVal.replaceAll('{{buttonSize}}', buttonSize);
    returnVal = returnVal.replaceAll('{{callToAction}}', callToAction);
    returnVal = returnVal.replaceAll('{{phoneNumber}}', phoneNumber);
    returnVal = returnVal.replaceAll('{{welcomeMessage}}', welcomeMessage);
    returnVal = returnVal.replaceAll('{{buttonIconSize}}', buttonIconSize);

    if (buttonMargin === 'true') {
        returnVal = returnVal.replaceAll(
            '{{buttonMargin}}',
            'wa-cta-button-label-margin',
        );
        returnVal = returnVal.replaceAll(
            '{{buttonPadding}}',
            'wa-button-size-with-words',
        );
    }

    if (buttonMargin === 'false') {
        returnVal = returnVal.replaceAll('{{buttonMargin}}', '');
        returnVal = returnVal.replaceAll('{{buttonPadding}}', '');
    }

    // insert markup into DOM
    document.querySelector('body').insertAdjacentHTML('beforeend', returnVal);

    // onClick for open and close whatsapp chat window
    document.getElementById('wa-cta-button').onclick = () => {
        const chatBox = document.querySelector('#wa-chat-window');

        const currentState = window.getComputedStyle(chatBox).display;
        if (currentState !== 'none') {
            return (chatBox.style.display = 'none');
        }
        return (chatBox.style.display = 'grid');
    };

    // whatsapp close button
    document.querySelector('#wa-close-btn').onclick = () => {
        const chatBox = document.querySelector('#wa-chat-window');
        chatBox.style.display = 'none';
    };
}
