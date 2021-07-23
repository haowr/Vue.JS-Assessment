<template>
  <div class="row">

<!-- NO CUSTOMERS FOUND MOBILE -->

    <div v-show="!tasks.length">
      <div class="item col s12 mobile center-align">
        <p class="grey-text lighten-2" style="padding-top: 50%">
          no customer(s) found with the search criteria.
        </p>
      </div>
    </div>

<!-- NO CUSTOMERS FOUND MOBILE -->

<!-- MAIN CUSTOMER LIST MOBILE -->

    <div
      class="col s12 mobile"
      style="border-radius: 10px; padding-bottom: 8rem"
      :key="task.id"
      v-for="task in tasks"
    >
      <div v-show="tasks.length" class="item col s12">
        <div class="col s6">
          <div class="task-subheader-mobile">
            <p style="font-size: 17px; font-weight: bold; padding-left: 1rem">
              {{ task.name }}
            </p>
            <p
              class="grey-text lighten-4"
              style="font-size: 13px; padding-left: 1rem"
            >
              @{{ task.username }}
            </p>
          </div>

          <div class="task-subheader-mobile"></div>
          <div class="task-subheader-mobile-catchphrase">
            <p
              class="blue-text lighten-2"
              style="font-size: 13px; padding-left: 1rem"
            >
              "{{ task.company.catchPhrase }}"
            </p>
          </div>
        </div>
        <div class="col s6">
          <div
            class="task-image"
            style="
              overflow: auto;
              padding-top: 24px;
              border-radius: 25px;
              border-radius: 25px;
            "
          >
            <img
              v-bind:src="pictures[task.id]"
              class=""
              style="height: 10rem"
              :alt="firstName"
            />
          </div>
        </div>

        <div class="col s12">
          <div class="task-subheader" style="padding-bottom: 10px">
            <i
              class="material-icons"
              style="
                font-size: 18px;
                padding-left: 1rem;
                color: rgb(39, 88, 133);
              "
              >email</i
            >
            <p
              style="
                font-size: 13px;
                padding-top: 5px;
                font-weight: 300;
                padding-left: 1rem;
              "
            >
              {{ task.email }}
            </p>
          </div>
          <div class="task">
            <i
              class="material-icons"
              style="
                font-size: 18px;
                padding-left: 1rem;
                color: rgb(39, 88, 133);
              "
              >add_location</i
            >
            <p
              style="
                font-size: 13px;
                padding-top: 5px;
                font-weight: 300;
                padding-left: 1rem;
              "
            >
              {{ task.address.street }},{{ task.address.suite }}
            </p>
          </div>
          <div class="task">
            <p
              style="
                font-size: 13px;
                padding-top: 5px;
                font-weight: 300;
                padding-left: 3.2rem;
              "
            >
              {{ task.address.city }},{{ task.address.zipcode }}
            </p>
          </div>
          <div class="task" style="padding-bottom: 10px">
            <p
              style="
                font-size: 13px;
                padding-top: 5px;
                font-weight: 300;
                padding-left: 3.2rem;
              "
            >
              {{ task.address.geo.lat }},{{ task.address.geo.lng }}
            </p>
          </div>
          <div class="task" style="padding-bottom: 10px">
            <i
              class="material-icons"
              style="
                font-size: 18px;
                padding-left: 1rem;
                color: rgb(39, 88, 133);
              "
              >local_phone</i
            >
            <p
              style="
                font-size: 13px;
                padding-top: 5px;
                font-weight: 300;
                padding-left: 1rem;
              "
            >
              {{ task.phone }}
            </p>
          </div>
          <div class="task" style="padding-bottom: 10px">
            <i
              class="material-icons"
              style="
                font-size: 18px;
                padding-left: 1rem;
                color: rgb(39, 88, 133);
              "
              >language</i
            >
            <p
              style="
                font-size: 13px;
                padding-top: 5px;
                font-weight: 300;
                padding-left: 1rem;
              "
            >
              {{ task.website }}
            </p>
          </div>
          <div class="task" style="padding-bottom: 10px">
            <i
              class="material-icons"
              style="
                font-size: 18px;
                padding-left: 1rem;
                color: rgb(39, 88, 133);
              "
              >card_travel</i
            >

            <p
              style="
                font-size: 13px;
                padding-top: 5px;
                font-weight: 300;
                padding-left: 1rem;
              "
            >
              {{ task.company.name }}
            </p>
          </div>
        </div>
      </div>

      <div v-show="!tasks.length" class="item col s12">
        <div class="col s6">
          <div class="task-subheader-mobile">
            <p style="font-size: 17px; font-weight: bold; padding-left: 1rem">
              {{ task.name }}
            </p>
            <p
              class="grey-text lighten-4"
              style="font-size: 13px; padding-left: 1rem"
            >
              @{{ task.username }}
            </p>
          </div>

          <div class="task-subheader-mobile"></div>
          <div class="task-subheader-mobile-catchphrase">
            <p
              class="blue-text lighten-2"
              style="font-size: 13px; padding-left: 1rem"
            >
              "{{ task.company.catchPhrase }}"
            </p>
          </div>
        </div>
        <div class="col s6">
          <div
            class="task-image"
            style="
              overflow: auto;
              padding-top: 24px;
              border-radius: 25px;
              border-radius: 25px;
            "
          >
            <img
              v-bind:src="pictures[task.id]"
              class=""
              style="height: 10rem"
              :alt="firstName"
            />
          </div>
        </div>

        <div class="col s12">
          <div class="task-subheader" style="padding-bottom: 10px">
            <i
              class="material-icons"
              style="
                font-size: 18px;
                padding-left: 1rem;
                color: rgb(39, 88, 133);
              "
              >email</i
            >
            <p
              style="
                font-size: 13px;
                padding-top: 5px;
                font-weight: 300;
                padding-left: 1rem;
              "
            >
              {{ task.email }}
            </p>
          </div>
          <div class="task">
            <i
              class="material-icons"
              style="
                font-size: 18px;
                padding-left: 1rem;
                color: rgb(39, 88, 133);
              "
              >add_location</i
            >
            <p
              style="
                font-size: 13px;
                padding-top: 5px;
                font-weight: 300;
                padding-left: 1rem;
              "
            >
              {{ task.address.street }},{{ task.address.suite }}
            </p>
          </div>
          <div class="task">
            <p
              style="
                font-size: 13px;
                padding-top: 5px;
                font-weight: 300;
                padding-left: 3.2rem;
              "
            >
              {{ task.address.city }},{{ task.address.zipcode }}
            </p>
          </div>
          <div class="task" style="padding-bottom: 10px">
            <p
              style="
                font-size: 13px;
                padding-top: 5px;
                font-weight: 300;
                padding-left: 3.2rem;
              "
            >
              {{ task.address.geo.lat }},{{ task.address.geo.lng }}
            </p>
          </div>
          <div class="task" style="padding-bottom: 10px">
            <i
              class="material-icons"
              style="
                font-size: 18px;
                padding-left: 1rem;
                color: rgb(39, 88, 133);
              "
              >local_phone</i
            >
            <p
              style="
                font-size: 13px;
                padding-top: 5px;
                font-weight: 300;
                padding-left: 1rem;
              "
            >
              {{ task.phone }}
            </p>
          </div>
          <div class="task" style="padding-bottom: 10px">
            <i
              class="material-icons"
              style="
                font-size: 18px;
                padding-left: 1rem;
                color: rgb(39, 88, 133);
              "
              >language</i
            >
            <p
              style="
                font-size: 13px;
                padding-top: 5px;
                font-weight: 300;
                padding-left: 1rem;
              "
            >
              {{ task.website }}
            </p>
          </div>
          <div class="task" style="padding-bottom: 10px">
            <i
              class="material-icons"
              style="
                font-size: 18px;
                padding-left: 1rem;
                color: rgb(39, 88, 133);
              "
              >card_travel</i
            >

            <p
              style="
                font-size: 13px;
                padding-top: 5px;
                font-weight: 300;
                padding-left: 1rem;
              "
            >
              {{ task.company.name }}
            </p>
          </div>
        </div>
      </div>
    </div>

<!-- MAIN CUSTOMER LIST MOBILE -->


<!-- NO CUSTOMERS FOUND DESKTOP -->

    <div v-show="!tasks.length">
      <div class="item col s12 desktop center-align">
        <p class="grey-text lighten-2" style="padding-top: 300px">
          no customer(s) found with the search criteria.
        </p>
      </div>
    </div>

<!-- NO CUSTOMERS FOUND DESKTOP -->

<!-- MAIN CUSTOMER LIST DESKTOP -->

    <div
      class="col s3 desktop"
      style="border-radius: 10px; padding-bottom: 8rem"
      :key="task.id"
      v-for="task in tasks"
    >
      <div class="item">
        <div class="task-image" style="overflow: auto">
          <img
            v-bind:src="pictures[task.id]"
            class=""
            style="border-radius: 10px; height: 20rem"
            :alt="firstName"
          />
        </div>
        <div class="task">
          <p style="font-size: 23px; font-weight: bold; padding-left: 1rem">
            {{ task.name }}
          </p>
        </div>

        <div class="task">
          <p
            class="grey-text lighten-4"
            style="font-size: 15px; padding-left: 1rem"
          >
            @{{ task.username }}
          </p>
        </div>
        <div class="task">
          <p
            class="blue-text lighten-2"
            style="font-size: 15px; padding-left: 1rem"
          >
            "{{ task.company.catchPhrase }}"
          </p>
        </div>
        <div class="task-subheader" style="padding-bottom: 10px">
          <i
            class="material-icons"
            style="font-size: 25px; padding-left: 1rem; color: rgb(39, 88, 133)"
            >email</i
          >
          <p
            style="
              font-size: 16px;
              padding-top: 5px;
              font-weight: 300;
              padding-left: 1rem;
            "
          >
            {{ task.email }}
          </p>
        </div>
        <div class="task">
          <i
            class="material-icons"
            style="font-size: 25px; padding-left: 1rem; color: rgb(39, 88, 133)"
            >add_location</i
          >
          <p
            style="
              font-size: 15px;
              padding-top: 5px;
              font-weight: 300;
              padding-left: 1rem;
            "
          >
            {{ task.address.street }},{{ task.address.suite }}
          </p>
        </div>
        <div class="task">
          <p
            style="
              font-size: 15px;
              padding-top: 5px;
              font-weight: 300;
              padding-left: 3.6rem;
            "
          >
            {{ task.address.city }},{{ task.address.zipcode }}
          </p>
        </div>
        <div class="task" style="padding-bottom: 10px">
          <p
            style="
              font-size: 15px;
              padding-top: 5px;
              font-weight: 300;
              padding-left: 3.6rem;
            "
          >
            {{ task.address.geo.lat }},{{ task.address.geo.lng }}
          </p>
        </div>
        <div class="task" style="padding-bottom: 10px">
          <i
            class="material-icons"
            style="font-size: 25px; padding-left: 1rem; color: rgb(39, 88, 133)"
            >local_phone</i
          >
          <p
            style="
              font-size: 15px;
              padding-top: 5px;
              font-weight: 300;
              padding-left: 1rem;
            "
          >
            {{ task.phone }}
          </p>
        </div>
        <div class="task" style="padding-bottom: 10px">
          <i
            class="material-icons"
            style="font-size: 25px; padding-left: 1rem; color: rgb(39, 88, 133)"
            >language</i
          >
          <p
            style="
              font-size: 15px;
              padding-top: 5px;
              font-weight: 300;
              padding-left: 1rem;
            "
          >
            {{ task.website }}
          </p>
        </div>
        <div class="task" style="padding-bottom: 10px">
          <i
            class="material-icons"
            style="font-size: 25px; padding-left: 1rem; color: rgb(39, 88, 133)"
            >card_travel</i
          >

          <p
            style="
              font-size: 15px;
              padding-top: 5px;
              font-weight: 300;
              padding-left: 1rem;
            "
          >
            {{ task.company.name }}
          </p>
        </div>
        <div class="task-text"></div>
      </div>
    </div>

<!-- MAIN CUSTOMER LIST DESKTOP -->

  </div>

</template>

<script>
//import Task from "./Task";

export default {
  name: "Tasks",
  props: ["sortType", "name"],
  watch: {
    name: async function (newVal, oldVal) {

      console.log("Prop changed: ", newVal, " | was: ", oldVal);

      if (newVal.length == 0) {

        console.log("empty");
        this.tasks = this.originalTasks;
      } else {
        this.tasks = await this.tasks.filter((item) => {
          if (item.name.indexOf(newVal) !== -1) {
            //this.tasks.push(item)
            //console.log(item.name)

            return item;
          }
        });
        console.log(this.tasks.length);
        if (this.tasks.length === 0) {
          this.noResultsOpen = true;
          console.log(this.noResultsOpen, "!!!!?");
        } else {
          this.noResultsOpen = false;
          console.log(this.noResultsOpen, "!!!!");
        }
      }
    },
    sortType: function (newVal, oldVal) {
      // watch it
      console.log("Prop changed: ", newVal, " | was: ", oldVal);

      //this.tasks.sort((a,b) => a[choice].localeCompare(b[choice]));
      if (newVal == 1) {
        this.tasks.sort(function (a, b) {
          if (a.name < b.name) {
            return -1;
          }
          if (a.name > b.name) {
            return 1;
          }
          return 0;
        });
      } else {
        this.tasks.sort(function (a, b) {
          if (a.name < b.name) {
            return 1;
          }
          if (a.name > b.name) {
            return -1;
          }
          return 0;
        });
      }
    },
  },
  components: {
  },
  data() {
    return {
      
      pictures: [
        "https://randomuser.me/api/portraits/men/1.jpg",
        "https://randomuser.me/api/portraits/men/2.jpg",
        "https://randomuser.me/api/portraits/men/3.jpg",
        "https://randomuser.me/api/portraits/men/4.jpg",
        "https://randomuser.me/api/portraits/men/5.jpg",
        "https://randomuser.me/api/portraits/men/6.jpg",
        "https://randomuser.me/api/portraits/men/7.jpg",
        "https://randomuser.me/api/portraits/men/8.jpg",
      ],
      tasks: [],
      noResultsOpen: true,
    };
  },
  methods() {},
  created() {
    //this.tasks =[];
    const fetchGif = async (tag) => {
      fetch("https://jsonplaceholder.typicode.com/users")
        .then((response) => response.json())
        .then(
          (data) => {
            console.log(data);
            this.tasks = data.slice(0, 8);
            this.originalTasks = data.slice(0, 8);
          } //console.log(data)
        );
    };
    fetchGif();
  },

  emits: [],
};
</script>
<style scoped>
.flex-container {
  position: relative;
  display: flex;
  flex-flow: row wrap;
  justify-content: space-between;
}
.item {
  flex: 1;
  flex-basis: 10%;
  height: 700px;
  padding-bottom: 20px;
  width: 300px;
  border-radius: 15px;
  background-color: white;
}
.task {
  display: flex;
  justify-content: left;
  background-color: white;
}
.task-subheader {
  display: flex;
  justify-content: left;
  background-color: white;
  padding-top: 30px;
}
.task-subheader-mobile-catchphrase {
  padding-top: 2px;
  background-color: white;
}
.task-subheader-mobile {
  padding-top: 20px;
  background-color: white;
}
.task-image {
  display: flex;
  justify-content: space-evenly;
  padding-bottom: 2rem;
}
.task-text {
  display: flex;
  justify-content: space-evenly;
}
.desktop {
  display: inline;
}
.mobile {
  display: none;
}

@media screen and (max-width: 1024px) {
  .item {
    display: inline;
    height: 450px;
  }
  .mobile {
    display: inline;
  }
  .desktop {
    display: none;
  }
}
</style>