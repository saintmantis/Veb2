<template>

  <v-carousel v-model="model" height = "100%">
    
    <v-carousel-item
      v-for="(item, i) in pictures"
      :key="i"
    >
      <v-sheet
      :color = "item.color"
        height="100%"
        tile
      >
        <v-row
          class="fill-height"
          align="center"
          justify="center"
        >
          <div class="display-1">
<v-card width="1000" class="mx-auto">
            <v-list-item>
                <v-list-item-content>
                        <v-img
                    :src="item.picture1"
                    >
                    </v-img>
                </v-list-item-content>
                <v-list-item-avatar size="400">
                    <v-img
                    :src="item.picture"
                    >
                    </v-img>
                </v-list-item-avatar>
                <v-list-item-action>
                </v-list-item-action>
            </v-list-item>
            <div>
                <Carusel v-show="Show"/>
            </div>
        </v-card>
          </div>
        </v-row>
      </v-sheet>
    </v-carousel-item>
  </v-carousel>
</template>

<script>
  export default {
    data: () => ({
      model: 0,
      Show: false,
      colors: [
        'primary',
        'secondary',
        'yellow darken-2',
        'red',
        'orange',
      ],
      pictures: [
          { picture:"https://golos.ua/images/items/2020-08/02/CxJ6myL6cfYB26Mn/img_top.jpg",
          picture1:"https://sun9-47.userapi.com/impg/gDRbscB60SiRf-SgXW9mt4BSQbM9eIXZE8zDUQ/digjVvwl0ys.jpg?size=453x239&quality=96&sign=0ce4ed2d11ee33e9de50f0b2fe367f68&type=album",
             color:"primary",
             text:""
          },
          {
            picture:"https://www.buro247.ua/thumb/670x830_0/images/2017/09/800-insta-of-the-week-sad-cat-luhu.jpg",
            picture1:"https://sun9-18.userapi.com/impg/iXVOO9SP44qMB11VZYasnMwNIB4w7sXuViwyXA/PloomXkKsoE.jpg?size=586x150&quality=96&sign=8cd8fecd1b1813b3202613930d5cf18a&type=album",
             color:"yellow",
             text:""
          },
          {
            picture:"https://rg.ru/img/content/155/62/15/RIAN_3266017.HR.ru_t_650x433.jpg",
            picture1:"https://sun9-72.userapi.com/impg/wFgrKaz5bTM6HJhErlIj1cl9ZUO8dxEC7YkDFQ/CSyRgeohfKI.jpg?size=554x170&quality=96&sign=d8105b4679195f6c89c7dc3d417194e5&type=album",
             color:"red",
             text:""
          },
          {
            picture:"https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQeAy1bWt8UI8W4-EhyuVzDPkRaPrF2DXMJ5A&usqp=CAU",
            picture1:"https://sun9-35.userapi.com/impg/g2iWoJCl945g2k-duXjie8TtZxXlZ1XftN3mMA/xy_kAqUGKk0.jpg?size=779x176&quality=96&sign=fd6e8fff02054f5828c3bba7036912e1&type=album",
             color:"green",
             text:""
          } 
          ]
    }),
  }
</script>