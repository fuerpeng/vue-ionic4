<template>
  <div>
  <ion-app>
    <ion-menu>
      <ion-header>
        <ion-toolbar color="primary">
          <ion-title>Menu</ion-title>
        </ion-toolbar>
      </ion-header>

      <ion-content>
        <ion-list>
          <ion-list-header>
            Navigate
          </ion-list-header>
          <ion-menu-toggle auto-hide="false">
            <ion-item button>
              <ion-icon slot="start" name='home'></ion-icon>
              <ion-label>
                Home
              </ion-label>
            </ion-item>
          </ion-menu-toggle>
        </ion-list>
      </ion-content>
    </ion-menu>

    <ion-page class="ion-page" main>
      <ion-header>
        <ion-toolbar>
          <ion-buttons slot="start">
            <ion-menu-toggle>
              <ion-button>
                <ion-icon slot="icon-only" name="menu"></ion-icon>
              </ion-button>
            </ion-menu-toggle>
          </ion-buttons>
          <ion-title>Header</ion-title>
        </ion-toolbar>
      </ion-header>
      <ion-tabs>

        <ion-tab tab="tab-one">
          <ion-header translucent>
            <ion-toolbar>
              <ion-title>Tab One</ion-title>
            </ion-toolbar>
          </ion-header>
          <ion-content padding fullscreen>
            <ion-button shape="round" color="primary" fill="outline">Hello World</ion-button>
            <ion-button size="small">Small Button</ion-button>
            <ion-checkbox color="primary" checked></ion-checkbox>
            <ion-checkbox color="secondary"></ion-checkbox>
            <ion-checkbox color="danger" checked></ion-checkbox>
            <ion-checkbox color="light"></ion-checkbox>
            <ion-checkbox color="dark" checked></ion-checkbox>
            <ion-item>
              <ion-label>Date</ion-label>
              <ion-datetime display-format="MM/DD/YYYY"></ion-datetime>
            </ion-item>

            <!-- fab placed to the bottom and start and on the bottom edge of the content overlapping footer with a list to the right -->
            <ion-fab vertical="bottom" horizontal="end" >
              <ion-fab-button>
                <ion-icon name="settings"></ion-icon>
              </ion-fab-button>
              <ion-fab-list side="top">
                <ion-fab-button><ion-icon name="logo-vimeo"></ion-icon></ion-fab-button>
                <ion-fab-button><ion-icon name="logo-facebook"></ion-icon></ion-fab-button>
                <ion-fab-button><ion-icon name="logo-googleplus"></ion-icon></ion-fab-button>
                <ion-fab-button><ion-icon name="logo-twitter"></ion-icon></ion-fab-button>
              </ion-fab-list>
            </ion-fab>

            <ion-grid>
              <ion-row>
                <ion-col>
                  ion-col
                </ion-col>
                <ion-col>
                  ion-col
                </ion-col>
                <ion-col>
                  ion-col
                </ion-col>
                <ion-col>
                  ion-col
                </ion-col>
              </ion-row>

              <ion-row>
                <ion-col size="6">
                  ion-col [size="6"]
                </ion-col>
                <ion-col>
                  ion-col
                </ion-col>
                <ion-col>
                  ion-col
                </ion-col>
              </ion-row>
            </ion-grid>
            <ion-item>
              <ion-label>Hair Color</ion-label>
              <ion-select value="brown" ok-text="Okay" cancel-text="Dismiss">
                <ion-select-option value="brown">Brown</ion-select-option>
                <ion-select-option value="blonde">Blonde</ion-select-option>
                <ion-select-option value="black">Black</ion-select-option>
                <ion-select-option value="red">Red</ion-select-option>
              </ion-select>
            </ion-item>
            <ion-slides pager="true">
              <ion-slide>
                <h1>Slide 1</h1>
              </ion-slide>

              <ion-slide>
                <h1>Slide 2</h1>
              </ion-slide>

              <ion-slide>
                <h1>Slide 3</h1>
              </ion-slide>
            </ion-slides>

            <ion-spinner></ion-spinner>
            <ion-spinner name="lines"></ion-spinner>
          </ion-content>
        </ion-tab>

        <ion-tab tab="tab-two">

          <ion-header translucent>
            <ion-toolbar>
              <ion-title>Tab Two</ion-title>
            </ion-toolbar>
          </ion-header>
          <ion-content padding fullscreen>
            <ion-action-sheet-controller></ion-action-sheet-controller>
            <ion-button expand="block" id="basic" @click="presentBasic">Basic</ion-button>
            <ion-button expand="block" id="noBackdropDismiss" @click="presentNoBackdropDismiss">No Backdrop Dismiss</ion-button>
            <ion-button expand="block" id="alertFromActionSheet" @click="presentAlert">Alert from Action Sheet</ion-button>
            <ion-button expand="block" id="scrollableOptions" @click="presentScroll">Scrollable Options</ion-button>
            <ion-button expand="block" id="scrollWithoutCancel" @click="presentScrollNoCancel">Scroll Without Cancel</ion-button>
            <ion-button expand="block" id="cancelOnly" @click="presentCancelOnly">Cancel Only</ion-button>
            <ion-button expand="block" id="icons" @click="presentIcons">Icons</ion-button>
            <ion-button expand="block" id="cssClass" @click="presentWithCssClass">Custom CSS Class</ion-button>



            <ion-alert-controller></ion-alert-controller>
            <ion-button id="basic" expand="block" @click="presentAlert()">Alert</ion-button>
            <ion-button id="longMessage" expand="block" @click="presentAlertLongMessage()">Alert Long Message</ion-button>
            <ion-button id="multipleButtons" expand="block" @click="presentAlertMultipleButtons()">Multiple Buttons (>2)</ion-button>
            <ion-button id="noMessage" expand="block" @click="presentAlertNoMessage()">Alert No Message</ion-button>
            <ion-button id="confirm" expand="block" @click="presentAlertConfirm()">Confirm</ion-button>
            <ion-button id="prompt" expand="block" @click="presentAlertPrompt()">Prompt</ion-button>
            <ion-button id="radio" expand="block" @click="presentAlertRadio()">Radio</ion-button>
            <ion-button id="checkbox" expand="block" @click="presentAlertCheckbox()">Checkbox</ion-button>
            <ion-button expand="block" @click="presentWithCssClass()">CssClass</ion-button>
          </ion-content>

        </ion-tab>

        <ion-tab tab="tab-three">

          <ion-header translucent>
            <ion-toolbar>
              <ion-title>Tab Three</ion-title>
            </ion-toolbar>
          </ion-header>
          <ion-content padding fullscreen>
            Tab Three
          </ion-content>

        </ion-tab>

        <ion-tab tab="tab-four" component="page-one"></ion-tab>

        <ion-tab-bar>
          <ion-tab-button tab="tab-one">
            <ion-label>Plain List</ion-label>
            <ion-icon name="star"></ion-icon>
          </ion-tab-button>

          <ion-tab-button tab="tab-two">
            <ion-label>Schedule</ion-label>
            <ion-icon name="globe"></ion-icon>
          </ion-tab-button>

          <ion-tab-button tab="tab-three">
            <ion-label>Stopwatch</ion-label>
            <ion-icon name="logo-facebook"></ion-icon>
          </ion-tab-button>

          <ion-tab-button tab="tab-four">
            <ion-label>Messages</ion-label>
            <ion-icon name="chatboxes"></ion-icon>
          </ion-tab-button>
        </ion-tab-bar>
      </ion-tabs>
    </ion-page>
    <ion-menu-controller></ion-menu-controller>

  </ion-app>
</div>
</template>

<script>
  export default {
    name: 'App',
    data() {
      return {
        items: [{id: 0, name: 'Ahmed'}, {id: 1, name: 'Naima'}]
      }
    },
    created(){
    },
    methods:{
      async presentBasic() {
        const mode = Ionic.mode;
        const actionSheetController = document.querySelector('ion-action-sheet-controller');
        await actionSheetController.componentOnReady();
        const actionSheetElement = await actionSheetController.create({
          header: "Albums",
          buttons: [{
            text: 'Delete',
            role: 'destructive',
            icon: 'trash',
            handler: () => {
              console.log('Delete clicked');
            }
          }, {
            text: 'Share',
            icon: 'share',
            handler: () => {
              console.log('Share clicked');
            }
          }, {
            text: 'Play (open modal)',
            icon: 'arrow-dropright-circle',
            handler: () => {
              console.log('Play clicked');
            }
          }, {
            text: 'Favorite',
            icon: mode === 'md' ? 'heart' : null,
            handler: () => {
              console.log('Favorite clicked');
            }
          }, {
            text: 'Cancel',
            icon: mode === 'md' ? 'close' : null,
            role: 'cancel',
            handler: () => {
              console.log('Cancel clicked');
            }
          }]
        });
        await actionSheetElement.present();
      },
      async presentIcons() {
        const mode = Ionic.mode;
        const actionSheetController = document.querySelector('ion-action-sheet-controller');
        await actionSheetController.componentOnReady();
        const actionSheetElement = await actionSheetController.create({
          header: "Albums",
          buttons: [{
            text: 'Delete',
            role: 'destructive',
            icon: 'trash',
            handler: () => {
              console.log('Delete clicked');
            }
          }, {
            text: 'Share',
            icon: 'share',
            handler: () => {
              console.log('Share clicked');
            }
          }, {
            text: 'Play (open modal)',
            icon: 'arrow-dropright-circle',
            handler: () => {
              console.log('Play clicked');
            }
          }, {
            text: 'Favorite',
            icon: 'heart',
            role: 'selected',
            handler: () => {
              console.log('Favorite clicked');
            }
          }, {
            text: 'Cancel',
            role: 'cancel',
            icon: 'close',
            handler: () => {
              console.log('Cancel clicked');
            }
          }]
        })
        await actionSheetElement.present();
      },
      async presentNoBackdropDismiss() {
        const actionSheetController = document.querySelector('ion-action-sheet-controller');
        await actionSheetController.componentOnReady();
        const actionSheetElement = await actionSheetController.create({
          backdropDismiss: false,
          buttons: [{
            text: 'Archive',
            handler: () => {
              console.log('Archive clicked');
            }
          }, {
            text: 'Destructive',
            role: 'destructive',
            handler: () => {
              console.log('Destructive clicked');
            }
          }, {
            text: 'Cancel',
            role: 'cancel',
            handler: () => {
              console.log('Cancel clicked');
            }
          }]
        });
        await actionSheetElement.present();
      },
      async presentAlert() {
        const actionSheetController = document.querySelector('ion-action-sheet-controller');
        await actionSheetController.componentOnReady();
        const actionSheetElement = await actionSheetController.create({
          buttons: [{
            text: 'Open Alert',
            handler: () => {
              console.log('Open Alert clicked');
            }
          }, {
            text: 'Cancel',
            role: 'cancel',
            handler: () => {
              console.log('Cancel clicked');
            }
          }]
        });
        await actionSheetElement.present();
      },
      async presentScroll() {
        const actionSheetController = document.querySelector('ion-action-sheet-controller');
        await actionSheetController.componentOnReady();
        const actionSheetElement = await actionSheetController.create({
          buttons: [
            {
              text: 'Add Reaction',
              handler: () => {
                console.log('Add Reaction clicked');
              }
            }, {
              text: 'Copy Text',
              handler: () => {
                console.log('Copy Text clicked');
              }
            }, {
              text: 'Share Text',
              handler: () => {
                console.log('Share Text clicked');
              }
            }, {
              text: 'Copy Link to Message',
              handler: () => {
                console.log('Copy Link to Message clicked');
              }
            }, {
              text: 'Remind Me',
              handler: () => {
                console.log('Remind Me clicked');
              }
            }, {
              text: 'Pin File',
              handler: () => {
                console.log('Pin File clicked');
              }
            }, {
              text: 'Star File',
              handler: () => {
                console.log('Star File clicked');
              }
            }, {
              text: 'Mark Unread',
              handler: () => {
                console.log('Mark Unread clicked');
              }
            }, {
              text: 'Edit Title',
              handler: () => {
                console.log('Edit Title clicked');
              }
            }, {
              text: 'Save Image',
              handler: () => {
                console.log('Save Image clicked');
              }
            }, {
              text: 'Copy Image',
              handler: () => {
                console.log('Copy Image clicked');
              }
            }, {
              text: 'Delete File',
              role: 'destructive',
              handler: () => {
                console.log('Delete File clicked');
              }
            }, {
              text: 'Cancel',
              role: 'cancel', // will always sort to be on the bottom
              handler: () => {
                console.log('Cancel clicked');
              }
            }
          ]
        });
        await actionSheetElement.present();
      },
      async presentScrollNoCancel() {
        const actionSheetController = document.querySelector('ion-action-sheet-controller');
        await actionSheetController.componentOnReady();
        const actionSheetElement = await actionSheetController.create({
          buttons: [
            {
              text: 'Add Reaction',
              handler: () => {
                console.log('Add Reaction clicked');
              }
            }, {
              text: 'Copy Text',
              handler: () => {
                console.log('Copy Text clicked');
              }
            }, {
              text: 'Share Text',
              handler: () => {
                console.log('Share Text clicked');
              }
            }, {
              text: 'Copy Link to Message',
              handler: () => {
                console.log('Copy Link to Message clicked');
              }
            }, {
              text: 'Remind Me',
              handler: () => {
                console.log('Remind Me clicked');
              }
            }, {
              text: 'Pin File',
              handler: () => {
                console.log('Pin File clicked');
              }
            }, {
              text: 'Star File',
              handler: () => {
                console.log('Star File clicked');
              }
            }, {
              text: 'Mark Unread',
              handler: () => {
                console.log('Mark Unread clicked');
              }
            }, {
              text: 'Edit Title',
              handler: () => {
                console.log('Edit Title clicked');
              }
            }, {
              text: 'Save Image',
              handler: () => {
                console.log('Save Image clicked');
              }
            }, {
              text: 'Copy Image',
              handler: () => {
                console.log('Copy Image clicked');
              }
            }, {
              text: 'Delete File',
              role: 'destructive',
              handler: () => {
                console.log('Delete File clicked');
              }
            }
          ]
        });
        await actionSheetElement.present();
      },
      async presentCancelOnly() {
        const actionSheetController = document.querySelector('ion-action-sheet-controller');
        await actionSheetController.componentOnReady();
        const actionSheetElement = await actionSheetController.create({
          buttons: [
            {
              text: 'Cancel',
              role: 'cancel', // will always sort to be on the bottom
              handler: () => {
                console.log('Cancel clicked');
              }
            }
          ]
        });
        await actionSheetElement.present();
      },
      async presentWithCssClass() {
        const actionSheetController = document.querySelector('ion-action-sheet-controller');
        await actionSheetController.componentOnReady();
        const actionSheetElement = await actionSheetController.create({
          header: "Custom Css Class",
          cssClass: "my-class my-custom-class",
          buttons: [
            {
              text: 'Test',
              role: 'test',
              cssClass: 'my-cancel-button my-custom-button customClass',
              handler: () => {
                console.log('Cancel clicked');
              }
            }
          ]
        });
        await actionSheetElement.present();
      },
      async presentAlert() {
        const alertController = document.querySelector('ion-alert-controller');
        await alertController.componentOnReady();
        const alert = await alertController.create({
          header: 'Alert',
          subHeader: 'Subtitle',
          message: 'This is an alert message.',
          buttons: ['OK']
        });
        return await alert.present();
      },
      async presentAlertLongMessage() {
        const alertController = document.querySelector('ion-alert-controller');
        await alertController.componentOnReady();
        const alert = await alertController.create({
          header: 'Alert',
          message: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum hendrerit diam lorem, a faucibus turpis sagittis eu. In finibus augue in dui varius convallis. Donec vulputate nibh gravida odio vulputate commodo. Suspendisse imperdiet consequat egestas. Nulla feugiat consequat urna eu tincidunt. Cras nec blandit turpis, eu auctor nunc. Pellentesque finibus, magna eu vestibulum imperdiet, arcu ex lacinia massa, eget volutpat quam leo a orci. Etiam mauris est, elementum at feugiat at, dictum in sapien. Mauris efficitur eros sodales convallis egestas. Phasellus eu faucibus nisl. In eu diam vitae libero egestas lacinia. Integer sed convallis metus, nec commodo felis. Duis libero augue, ornare at tempus non, posuere vel augue. Cras mattis dui at tristique aliquam. Phasellus fermentum nibh ligula, porta hendrerit ligula elementum eu. Suspendisse sollicitudin enim at libero iaculis pulvinar. Donec ac massa id purus laoreet rutrum quis eu urna. Mauris luctus erat vel magna porttitor, vel varius erat rhoncus. Donec eu turpis vestibulum, feugiat urna id, gravida mauris. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer at lobortis tortor. Nam ultrices volutpat elit, sed pharetra nulla suscipit at. Nunc eu accumsan eros, id auctor libero. Suspendisse potenti. Nam vitae dapibus metus. Maecenas nisi dui, sagittis et condimentum eu, bibendum vel eros. Vivamus malesuada, tortor in accumsan iaculis, urna velit consectetur ante, nec semper sem diam a diam. In et semper ante. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus blandit, velit vel porttitor euismod, neque risus blandit nulla, non laoreet libero dolor et odio. Nulla enim risus, feugiat eu urna sed, ultrices semper felis. Sed blandit mi diam. Nunc quis mi ligula. Pellentesque a elit eu orci volutpat egestas. Aenean fermentum eleifend quam, ut tincidunt eros tristique et. Nam dapibus tincidunt ligula, id faucibus felis sodales quis. Donec tincidunt lectus ipsum, ac semper tellus cursus ac. Vestibulum nec dui a lectus accumsan vestibulum quis et velit. Aliquam finibus justo et odio euismod, viverra condimentum eros tristique. Sed eget luctus risus. Pellentesque lorem magna, dictum non congue sodales, laoreet eget quam. In sagittis vulputate dolor a ultricies. Donec viverra leo sed ex maximus, in finibus elit gravida. Aliquam posuere vulputate mi. Suspendisse potenti. Nunc consectetur congue arcu, at pharetra dui varius non. Etiam vestibulum congue felis, id ullamcorper neque convallis ultrices. Aenean congue, diam a iaculis mollis, nisl eros maximus arcu, nec hendrerit purus felis porta diam. Nullam vitae ultrices dui, ac dictum sapien. Phasellus eu magna luctus, varius urna id, molestie quam. Nulla in semper tellus. Curabitur lacinia tellus sit amet lacinia dapibus. Sed id condimentum tellus, nec aliquam sapien. Vivamus luctus at ante a tincidunt.',
          buttons: ['Cancel', 'OK']
        });
        return await alert.present();
      },
      async presentAlertMultipleButtons() {
        const alertController = document.querySelector('ion-alert-controller');
        await alertController.componentOnReady();
        const alert = await alertController.create({
          header: 'Alert',
          subHeader: 'Subtitle',
          message: 'This is an alert message.',
          buttons: ['Cancel', 'Open Modal', 'Delete']
        });
        return await alert.present();
      },
      async presentAlertNoMessage() {
        const alertController = document.querySelector('ion-alert-controller');
        await alertController.componentOnReady();
        const alert = await alertController.create({
          header: 'Alert',
          buttons: ['OK']
        });
        return await alert.present();
      },
      async presentAlertConfirm() {
        const alertController = document.querySelector('ion-alert-controller');
        await alertController.componentOnReady();
        const alert = await alertController.create({
          header: 'Confirm!',
          message: 'Message <strong>text</strong>!!!',
          buttons: [
            {
              text: 'Cancel',
              role: 'cancel',
              cssClass: 'secondary',
              handler: (blah) => {
                console.log('Confirm Cancel: blah');
              }
            }, {
              text: 'Okay',
              handler: () => {
                console.log('Confirm Okay')
              }
            }
          ]
        });
        return await alert.present();
      },
      async presentAlertPrompt() {
        const alertController = document.querySelector('ion-alert-controller');
        await alertController.componentOnReady();
        const alert = await alertController.create({
          header: 'Prompt!',
          inputs: [
            {
              placeholder: 'Placeholder 1'
            },
            {
              name: 'name2',
              id: 'name2-id',
              value: 'hello',
              placeholder: 'Placeholder 2'
            },
            {
              name: 'name3',
              value: 'http://ionicframework.com',
              type: 'url',
              placeholder: 'Favorite site ever'
            },
            // input date with min & max
            {
              name: 'name4',
              type: 'date',
              min: '2017-03-01',
              max: '2018-01-12'
            },
            // input date without min nor max
            {
              name: 'name5',
              type: 'date'
            },
            {
              name: 'name6',
              type: 'number',
              min: -5,
              max: 10
            },
            {
              name: 'name7',
              type: 'number'
            }
          ],
          buttons: [
            {
              text: 'Cancel',
              role: 'cancel',
              cssClass: 'secondary',
              handler: () => {
                console.log('Confirm Cancel')
              }
            }, {
              text: 'Ok',
              handler: () => {
                console.log('Confirm Ok')
              }
            }
          ]
        });
        return await alert.present();
      },
      async presentAlertRadio() {
        const alertController = document.querySelector('ion-alert-controller');
        await alertController.componentOnReady();
        const alert = await alertController.create({
          header: 'Radio',
          inputs: [
            {
              type: 'radio',
              label: 'Radio 1',
              name: 'Radio 1',
              value: 'value1',
              checked: true
            },
            {
              type: 'radio',
              label: 'Radio 2',
              name: 'Radio 2',
              value: 'value2'
            },
            {
              type: 'radio',
              label: 'Radio 3',
              name: 'Radio 3',
              value: 'value3'
            },
            {
              type: 'radio',
              label: 'Radio 4',
              name: 'Radio 4',
              value: 'value4'
            },
            {
              type: 'radio',
              label: 'Radio 5',
              name: 'Radio 5',
              value: 'value5'
            },
            {
              type: 'radio',
              label: 'Radio 6 Radio 6 Radio 6 Radio 6 Radio 6 Radio 6 Radio 6 Radio 6 Radio 6 Radio 6 ',
              name: 'Radio 6',
              value: 'value6'
            }
          ],
          buttons: [
            {
              text: 'Cancel',
              role: 'cancel',
              cssClass: 'secondary',
              handler: () => {
                console.log('Confirm Cancel')
              }
            }, {
              text: 'Ok',
              handler: () => {
                console.log('Confirm Ok')
              }
            }
          ]
        });
        return await alert.present();
      },
      async presentAlertCheckbox() {
        const alertController = document.querySelector('ion-alert-controller');
        await alertController.componentOnReady();
        const alert = await alertController.create({
          header: 'Checkbox',
          inputs: [
            {
              type: 'checkbox',
              label: 'Checkbox 1',
              name: 'Checkbox 1',
              value: 'value1',
              checked: true
            },
            {
              type: 'checkbox',
              label: 'Checkbox 2',
              name: 'Checkbox 2',
              value: 'value2'
            },
            {
              type: 'checkbox',
              label: 'Checkbox 3',
              name: 'Checkbox 3',
              value: 'value3'
            },
            {
              type: 'checkbox',
              label: 'Checkbox 4',
              name: 'Checkbox 4',
              value: 'value4'
            },
            {
              type: 'checkbox',
              label: 'Checkbox 5',
              name: 'Checkbox 5',
              value: 'value5'
            },
            {
              type: 'checkbox',
              label: 'Checkbox 6 Checkbox 6 Checkbox 6 Checkbox 6 Checkbox 6 Checkbox 6 Checkbox 6 Checkbox 6 Checkbox 6 Checkbox 6',
              name: 'Checkbox 6',
              value: 'value6'
            }
          ],
          buttons: [
            {
              text: 'Cancel',
              role: 'cancel',
              cssClass: 'secondary',
              handler: () => {
                console.log('Confirm Cancel')
              }
            }, {
              text: 'Ok',
              handler: () => {
                console.log('Confirm Ok')
              }
            }
          ]
        });
        return await alert.present();
      },
      async presentWithCssClass() {
        const alertController = document.querySelector('ion-alert-controller');
        await alertController.componentOnReady();
        const alert = await alertController.create({
          header: 'Alert',
          subHeader: 'Subtitle',
          cssClass: 'my-class my-customClass   ',
          message: 'This is an alert message.',
          buttons: [{
            text: 'Ok',
            cssClass: 'my-class my-customClass   ',
            handler: () => {
              console.log('Confirm Ok')
            }
          }]
        });
        return await alert.present();
      }
    }
  }
</script>
<style>
  .show-page {
    min-height: 100%;
  }
</style>
