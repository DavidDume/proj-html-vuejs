<template>

    <div class="live-dates title">
        <h1>Live Dates</h1>
        <div class="bottom-bar"></div>
        <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Ratione similique sit quam, eum placeat maxime. Nihil corporis 
        </p>

        <div class="dates">
            <div class="date" v-for="(date, index) in dates" >

                <i class="fa-solid fa-plus" v-show="showDate==null"></i>

                <i class="fa-solid fa-minus pointer" @click="showDate=null" v-show="showDate==index"></i>

                <h3 class="pointer" @click="showDate=index">{{ date.title }}</h3>

                <div class="date-details" v-show="showDate==index">
                    <img src="../assets/maps.png" alt="">
                    <div class="details-text">
                        <h4>Untold Stories</h4>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ratione similique sit quam, eum placeat maxime. Nihil corporis </p>
                        <button class="red-btn pointer">Book Now</button>
                    </div>
                </div>

            </div>
        </div>
    </div>

</template>

<script>

    export default {
        name: 'LiveDates',
        data() {
            return {
                dates: [
                    {
                        title: '17/08/2020 Gem festival 2020 anakalia, georgia',
                        subtitle: 'Untold Stories',
                        desc: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Ratione similique sit quam, eum placeat maxime. Nihil corporis'
                    },
                    {
                        title: '24/9/2020 CROOVEFEST DOMINICAL REPUBLIC',
                        subtitle: 'Untold Stories',
                        desc: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Ratione similique sit quam, eum placeat maxime. Nihil corporis'
                    },
                    {
                        title: '31/10/2020 OASIS FESTIVAL 2020 MARRAKECH, MOROCCO',
                        subtitle: 'Untold Stories',
                        desc: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Ratione similique sit quam, eum placeat maxime. Nihil corporis'
                    },
                    {
                        title: '07/11/2020 MOCA FESTIVAL - ESSAOURIA, MOROCCO',
                        subtitle: 'Untold Stories',
                        desc: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Ratione similique sit quam, eum placeat maxime. Nihil corporis'
                    },
                    {
                        title: '10/12/2020 ENVISION FESTIVAl - UVITA, COSTA RICA',
                        subtitle: 'Untold Stories',
                        desc: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Ratione similique sit quam, eum placeat maxime. Nihil corporis'
                    },
                ],
                showDate: null
            }
        }
    }

</script>

<style lang="scss">
    @use '../styles/variables' as *;

    .date-details {
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 20px;
        margin-top: 10px;
        & img {
            width: 200px;
        }
        & h4 {
            font-weight: 300;
            letter-spacing: 1px;
            color: white;
            font-size: 15px;
        }
        & p {
            margin: 0;
            padding: 20px 0;
            line-height: 25px;
        }
        & button {
            padding: 5px 10px;
            color: white;
            border: none;
        }
    }

    .live-dates {
        padding: 70px 0 80px 0;
    }
    .date {
        background-color: #323844;
        color: $red;
        margin-top: 5px;
        padding: 15px;
        text-align: left;
        & i {
            color: white;
            font-size: 8px;
            vertical-align: middle;
            margin: 0 15px;
        }
        & h3 {
            font-size: 12px;
            text-transform: uppercase;
            font-weight: 300;
            letter-spacing: 1px;
            display: inline-block;
        }
    }

</style>