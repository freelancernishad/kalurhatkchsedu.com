<template>
    <div>

        <loader v-if="preloader" object="#ff9633" color1="#ffffff" color2="#17fd3d" size="25" speed="2"
            bg="#343a40" objectbg="#999793" opacity="80" disableScrolling="false" name="loading"></loader>

<section class="inner-header divider layer-overlay overlay-theme-colored-7" >
<div class="container">
    <!-- Section Content -->
    <div class="section-content">
        <div class="row">
            <div class="col-md-6">
                <h1 class="text-theme-colored2 font-36"> অধ্যয়নরত শিক্ষার্থীর সংখ্যা</h1>
                <ol class="breadcrumb text-left mt-10 white">
                    <li><a href="">Home</a></li>
                    <li class="active">student_at_a_glance</li>
                </ol>
            </div>
        </div>
    </div>
</div>
</section>


 <!-- Main Start -->
    <main class="container-fluid">
        <div class="row">
            <!-- Left Main -->
            <div class="col-lg-9 my-3">
            <div class="container">

    <table cellpadding="3" cellspacing="0" style="margin: 0 auto;margin-top: 22px;" width="100%">

        <tr>
            <td class="columnStyleLeft">
                <div>
                    <table cellspacing="0" cellpadding="3" id="ContentPlaceHolder1_grdvTeachers" style="font-family:Noto Sans Bengali;font-size:11pt;border-collapse:collapse;margin: 0 auto;width:100%">
                        <tr align="center" valign="middle" style="color:#0C090A;background-color:#F2F2F2;border-color:#CCCCCC;border-width:1px;border-style:Solid;font-family:Noto Sans Bengali;font-size:9pt;">
                            <td colspan="1" style="border-width:0px;text-align: center;">শ্রেণী</td>
                            <td colspan="3" style="border-color:#CCCCCC;border-width:1px;border-style:Solid;text-align: center;">শিক্ষার্থী</td>
                            <td colspan="3" style="border-color:#CCCCCC;border-width:1px;border-style:Solid;text-align: center;">বিভাগ</td>
                        </tr>
                        <tr align="center" valign="middle" style="color:#0C090A;background-color:#F2F2F2;border-color:#CCCCCC;border-width:1px;border-style:Solid;font-family:Noto Sans Bengali;font-size:9pt;">
                            <td align="left" valign="middle" scope="col"></td>
                            <td align="center" valign="middle" scope="col" style="border-color:#CCCCCC;border-width:1px;border-style:Solid;">ছাত্র</td>
                            <td align="center" valign="middle" scope="col" style="border-color:#CCCCCC;border-width:1px;border-style:Solid;">ছাত্রী</td>
                            <td align="center" valign="middle" scope="col" style="border-color:#CCCCCC;border-width:1px;border-style:Solid;">মোট</td>
                            <td align="center" valign="middle" scope="col" style="border-color:#CCCCCC;border-width:1px;border-style:Solid;">বিজ্ঞান</td>
                            <!-- <th align="center" valign="middle" scope="col" style="border-color:#CCCCCC;border-width:1px;border-style:Solid;">ব্যব.শি</th> -->
                            <td align="center" valign="middle" scope="col" style="border-color:#CCCCCC;border-width:1px;border-style:Solid;">মানবিক</td>
                        </tr>

                        <tr v-for="(student,key) in students.data">
                            <td align="center" style="border-color:#CCCCCC;border-width:1px;border-style:Solid;font-family:Century Gothic;font-size:9pt;width:75px;">{{ key }}</td>
                            <td align="center" style="border-color:#CCCCCC;border-width:1px;border-style:Solid;font-size:9pt;width:30px;">
                                <span id="ContentPlaceHolder1_grdvTeachers_txtmale_0">{{ student.maleStudent }}</span>
                            </td>
                            <td align="center" style="border-color:#CCCCCC;border-width:1px;border-style:Solid;font-size:9pt;width:30px;">
                                <span id="ContentPlaceHolder1_grdvTeachers_txtfemale_0">{{ student.FemaleStudent }}</span>
                            </td>
                            <td align="center" style="border-color:#CCCCCC;border-width:1px;border-style:Solid;font-size:9pt;width:30px;">
                                <span id="ContentPlaceHolder1_grdvTeachers_txttotal_0">{{ student.totalStudent }}</span>
                            </td>
                            <td align="center" style="border-color:#CCCCCC;border-width:1px;border-style:Solid;font-size:9pt;width:30px;">
                                <span id="ContentPlaceHolder1_grdvTeachers_txtmuslim_0">{{ student.scienceStudent }}</span>
                            </td>

                            <!-- <td align="center" style="border-color:#CCCCCC;border-width:1px;border-style:Solid;font-size:9pt;width:30px;">
                                <span id="ContentPlaceHolder1_grdvTeachers_txthindu_0">{{ student.CommerceStudent }}</span>
                            </td> -->

                            <td align="center" style="border-color:#CCCCCC;border-width:1px;border-style:Solid;font-size:9pt;width:30px;">
                                <span id="ContentPlaceHolder1_grdvTeachers_txtbouddho_0">{{ student.HumanitiesStudent }}</span>
                            </td>
                        </tr>

                    </table>
                </div>
                <div>
                    <table cellspacing="0" cellpadding="0" id="ContentPlaceHolder1_grdvTotal" style="width: 250px;border-collapse:collapse;margin: 0 auto;">
                        <tr>
                            <td scope="col">&nbsp;</td>
                        </tr>
                        <tr>
                            <td>
                                <table width="100%" cellpadding="2" cellspacing="0">



                                    <tr  v-for="(student,key) in students.countdata">
                                        <td class="firstColumn" style="border-top: 1px solid #CCCCCC;">
                                            {{ key }}
                                        </td>
                                        <td colspan="3" class="secondColumn" style="border-top: 1px solid #CCCCCC;">
{{ student }}
                                        </td>
                                    </tr>
                                </table>
                            </td>
                        </tr>
                    </table>
                </div>
            </td>
        </tr>
    </table>

    <!-- <adsense ad-client="ca-pub-9489624253487221" ad-format="fluid" ad-slot="4940322175" ad-layout-key="-fb+5w+4e-db+86"></adsense> -->




</div>
            </div>

            <side-bar class-name="col-md-3"></side-bar>


        </div>
    </main>
    <!-- Main End -->


    </div>
</template>

<script>


export default {

	created(){

  this.ASSETURL = ASSETURL
	},

	data () {
		return {
            students: {},

            ASSETURL: '',
            preloader: true,
		}
	},

	methods: {

        getstudentsData(){
            axios.get(`/api/student_at_a_glance?school_id=${this.school_id}&front=front`)
                .then(({ data }) => {
                    this.students = data;
                     this.preloader = false;
                })
                .catch()
        },



	},
	mounted(){

this.getstudentsData()

	}
}
</script>

<style>



.mini-profile-widget .image-container .avatar {
    width: 180px;
    height: 180px;
    display: block;
    margin: 0 auto;
    border-radius: 50%;
    background: white;
    padding: 4px;
    border: 1px solid #dddddd;
}


</style>
