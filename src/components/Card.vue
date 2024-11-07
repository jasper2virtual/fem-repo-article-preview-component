<template>
    <div
        class="max-w-[327px] desktop:max-w-[730px] rounded-lg shadow-lg bg-white
        flex flex-col gap-6 
        desktop:grid desktop:grid-cols-[285px_1fr]">

        <!-- header -->
        <div class="rounded-t-lg bg-[url('/src/assets/images/drawers.jpg')] bg-cover
        min-h-[200px] desktop:min-h-fit
        desktop:rounded-t-none desktop:rounded-l-lg desktop:row-span-2
        ">
        </div>

        <!-- body -->
        <div class="flex flex-col gap-4 p-8">



                <p class="font-bold text-xl text-very-dark-grayish-blue">
                    Shift the overall look and feel by adding these wonderful
                    touches to furniture in your home
                </p>

                <p class="font-medium text-desaturated-dark-blue">
                    Ever been in a room and felt like something was missing? Perhaps
                    it felt slightly bare and uninviting. I’ve got some simple tips
                    to help you make any room feel complete.
                </p>




        </div>
        
        <!-- footer : mobile version-->
        <div :class="['flex desktop:hidden px-8 h-20', showMobileShare && 'bg-very-dark-grayish-blue rounded-b-lg']">

            <Author v-if="!showMobileShare" authorName="Michelle Appleton" updateDate="28 Jun 2020"
                avatar="avatar-michelle.jpg" />

            <div v-if="showMobileShare" class="col-span-2 row-span-2 self-center">
                <ShareButtons />
            </div>

            <button
                :class="['rounded-full aspect-square shadow-sm ml-auto hover:bg-grayish-blue p-3 self-center',
                showMobileShare ? 'bg-desaturated-dark-blue':'bg-light-grayish-blue ']"
                @click="switchShowMobileShare">
                <IconShare :fill="showMobileShare && '#ffffff'"/>
            </button>
        </div>

        <!-- footer : desktop version -->
         <div class="hidden desktop:flex p-8">
            <Author authorName="Michelle Appleton" updateDate="28 Jun 2020"
                avatar="avatar-michelle.jpg" />
            

            <button
                :class="['relative rounded-full aspect-square shadow-sm ml-auto hover:bg-grayish-blue p-3 self-center',
                        showDesktopShare?'bg-desaturated-dark-blue':'bg-light-grayish-blue']"
                @click="switchShowDesktopShare">
                <div v-if="showDesktopShare"
                class="absolute -top-16 -left-24 flex flex-col items-center">
                    <ShareButtons class="bg-very-dark-grayish-blue rounded-lg px-4 py-2 shadow-lg"/>
                    <div class="border border-t-[1rem] border-l-[.5rem] border-r-[.5rem]
                    border-t-very-dark-grayish-blue
                    border-l-very-dark-grayish-blue/0 border-r-very-dark-grayish-blue/0
                    "></div>
                </div>
                <IconShare :fill="showDesktopShare && '#ffffff'"/>
                
            </button>

         </div>
    </div>
</template>
<script>
import ShareButtons from './ShareButtons.vue'
import Author from './Author.vue'
import IconShare from './IconShare.vue'
export default {
    components: {
        ShareButtons,
        Author,
        IconShare
    },
    data() {
        return {
            showMobileShare: false,
            showDesktopShare: false
        }
    },
    methods: {
        switchShowMobileShare() {
            this.showMobileShare = !this.showMobileShare
        },
        switchShowDesktopShare() {
            this.showDesktopShare = !this.showDesktopShare
        }
    }
}
</script>