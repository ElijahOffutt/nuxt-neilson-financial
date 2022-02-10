<template>
    <footer :style="`background-color: ${primary}`">
        <v-row class="pt-10 pb-8" style="width: 1180px; margin: 0 auto;">
            <v-col cols="4">
                <img height="50px" src="https://www.neilsonfs.com/media/kkldw1ei/neilson-fs-white.png" />
            </v-col>
            <v-col>
                <v-list style="background-color: transparent;">
                    <v-list-item v-for="(link, i) in links"  :key="i">
                        <v-list-item-avatar>
                            <v-icon :color="link.color">mdi-{{link.icon}}</v-icon>
                        </v-list-item-avatar>
                        <v-list-item-content>
                            <v-list-item-title>
                                <a style="color: white; text-decoration: none;" :href="link.link" target="blank">
                                    {{link.text}}
                                </a>
                            </v-list-item-title>
                        </v-list-item-content>
                    </v-list-item>
                </v-list>
            </v-col>
            <v-col class="shrink">
                <v-btn tag="a" href="https://www.linkedin.com/company/neilson-financial-services/" fab small color="white"><v-icon>mdi-linkedin</v-icon></v-btn>
            </v-col>
            <v-col cols="12">
                <p style="color: white; text-align: center; font-size: .8em;">Neilson Financial Services Limited is authorised and regulated by the Financial Conduct Authority and entered on the Financial Services Register under reference 594926. Registered Office: 2 Windsor Dials, Arthur Road, Windsor, SL4 1RS. Registered in England and Wales, number 07986483. Neilson Financial Services Inc. is incorporated and registered in Alberta whose registered office is at 850 - 2nd Street SW, 15th Floor, Bankers Court, Calgary, Alberta T2P 0R8. </p>
                <p class="bottomLinks" style="color: white; text-align: center; font-size: .8em;">
                    <a style="color: white; text-decoration: none;" href="https://www.neilsonfs.com/legals/privacy-policy/">Privacy Policy</a> | 
                    <a style="color: white; text-decoration: none;" href="https://www.neilsonfs.com/legals/cookie-policy/">Cookie Policy</a> | 
                    <a style="color: white; text-decoration: none;" href="https://www.neilsonfs.com/legals/complaints/">Complaints</a>
                </p>
            </v-col>
        </v-row>
    </footer>
</template>

<script>

let colors = require('../assets/colors.json');

export default {
    data(){return{
        primary: colors.primary,
        links: [
                {
                    text: '2 Windsor Dials, Arthur Road, Windsor SL4 1RS ',
                    link: 'https://www.google.com/maps/place/Windsor+Dials/@51.483133,-0.6144067,17z/data=!3m1!4b1!4m5!3m4!1s0x48767ae2bd9e0243:0x51e1e0839315282a!8m2!3d51.4829315!4d-0.6122826?shorturl=1',
                    icon: 'map-marker',
                    color: colors.accent
                },
                {
                    text: '1500, 850 2 Street SW, Calgary, AB, T2P 0R8, Canada ',
                    link: 'https://opencorporates.com/companies/ca_nl/88218',
                    icon: 'map-marker',
                    color: colors.accent
                },
                {
                    text: 'enquiries@neilsonfs.com ',
                    link: 'enquiries@neilsonfs.com',
                    icon: 'email',
                    color: colors.secondary
                }
            ]
    }}
}
</script>