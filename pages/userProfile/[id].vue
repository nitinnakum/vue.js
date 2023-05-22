<template>
    <div>
        <userLocation :userLocation="user.location" :userProfileImage="user.profileImage" :userHadding="user.userHadding"
            :userHaddingName="user.userHaddingName" :userBasicDetails="user.basicDetails" />
    </div>
    <div class="mt-7 ">
        <addisinalDetail :details="user.additionalDetails"
            :detailsActivitiesDevices="user.additionalDetails.ActivitiesDevices"
            :detailsAddtionalActivities="user.additionalDetails.ActivitiesDevices" />
    </div>
    <div class="mt-7">
        <userActivities :userActivities="user.activities" />
    </div>
    <div>
        <notes />
    </div>
</template>
<script>
import componentsUserImage from "~/components/user/image.vue"
import componentUserDetail from "~/components/user/detail.vue"
import componentsUserNotes from "~/components/user/notes.vue"
import componentsUserDetailActivities from "~/components/user/detailActivities.vue"
export default {
    name: "userProfileDetail",
    components: { "userLocation": componentsUserImage, "addisinalDetail": componentUserDetail, "userActivities": componentsUserDetailActivities, "notes" : componentsUserNotes },
    data() {
        return {
            user: {
                location: "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d117977.4631259921!2d69.97601164964335!3d22.47430951915293!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3957154934c04597%3A0xe8b7dd81a49b75ca!2sJamnagar%2C%20Gujarat!5e0!3m2!1sen!2sin!4v1682405457814!5m2!1sen!2sin",

                profileImage: "http://starsunfolded.com/wp-content/uploads/2017/03/Rhea-Sharma.jpg",

                userHadding: {
                    UserName: "Misti2.o"
                },

                userHaddingName: {
                    FullName: "Reha sharma"
                },

                basicDetails: {
                    UserGroup: "Active loyal",
                    Role: "Member",
                    Email: "misti1995@gmail.com",
                    DateRegister: "August 07, 2022",
                    LifeTimeValue: "429.88"
                },

                additionalDetails: {
                    ActivitiesDevices: {
                        LastSeen: "4 days ago",
                        Session: "25",
                        Browser: "Firefox",
                        Platform: "Apple"
                    },
                    Location: {
                        Country: "India",
                        City: "Jamnagar",
                        Region: "Shekhpat"
                    },
                    PersonalInfo: {
                        BorthOfDate: "November 26 2000",
                        PhoneNumber: "6353696190",
                        JobTitle: "Web Devloper"
                    }
                },
                activities: [
                    {
                        icon: "https://w7.pngwing.com/pngs/257/813/png-transparent-hamburger-button-computer-icons-menu-navigation-angle-white-text-thumbnail.png",
                        title: "2 posts",
                        data: [{
                            title: "flex Box is best working tools of css"
                        },
                        {
                            title: "that is use for html in avalable content is movment work for esaly"
                        }
                        ]
                    },
                    {
                        icon: "https://w7.pngwing.com/pngs/257/813/png-transparent-hamburger-button-computer-icons-menu-navigation-angle-white-text-thumbnail.png",
                        title: "3 potst comment",
                        data: [
                            {
                                title: "flex Box is best working tools of css"
                            },
                            {
                                title: "that is use for html in avalable content is movment work for esaly"
                            },
                            {
                                title: "tha is best tools of css property"
                            },
                        ]
                    },
                    {
                        icon: "https://st2.depositphotos.com/3867453/11100/v/950/depositphotos_111004120-stock-illustration-letter-w-logo-icon-design.jpg",
                        title: "3 orders",
                        data: [
                            {
                                title: "#3878 April 8, 2019-$15000",
                                states: "pending",
                                other: "Gift Card"
                            },
                            {
                                title: "#3475 March 8, 2018-$15000",
                                states: "Completed",
                                other: "Walk planner"
                            },
                            {
                                title: "#1372 January 3, 2016-$15000",
                                states: "Completed",
                                other: "Premium pents - Limited Editing"
                            }
                        ]
                    },
                    {
                        icon: "https://w7.pngwing.com/pngs/304/504/png-transparent-index-finger-pointer-computer-icons-symbol-fingertip-miscellaneous-text-hand.png",
                        title: "Last Visited Pages",
                        data: [
                            {
                               title : "Upcoming Events"
                            },
                            {
                                title : "Css Online Course"
                            },
                           {
                               title : "Shop"
                           },
                           {
                               title : "My Account"
                           }
                        ]
                    }
                ],
                notes: [
                    {
                        note: "I Had a with like new Profile",
                        user_name: "Admin",
                        created_at: "April 12, 2019"
                    },
                    {
                        note: "I like so much this device",
                        user_name: "Admin",
                        created_at: "june 23, 2020"
                    },
                    {
                        note: "I am profesonal web devloper",
                        user_name: "Admin",
                        created_at: "May 5, 2020"
                    }
                ]
            }
        }
    }
}
</script>
<style></style>