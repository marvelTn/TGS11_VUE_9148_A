<template>
  <v-app id="inspire">
    <v-content>
      <v-container class="fill-height" fluid>
        <v-row align="center" justify="center">
          <v-col cols="12" sm="8" md="4">
            <v-card class="elevation-12">
              <v-toolbar color="primary" dark flat>
                <v-toolbar-title>Login form</v-toolbar-title>
                <v-spacer />
              </v-toolbar>
              <v-card-text>
                <v-form>
                  <v-text-field label="Login" icon name="login" type="text" />
                  <v-text-field id="password" label="Password" name="password" type="password" />
                </v-form>
              </v-card-text>
              <v-card-actions>
                <v-spacer />
                <v-btn
                  v-for="item in items"
                  :key="item.text"
                  router
                  :to="item.route"
                  color="primary"
                >{{item.text}}</v-btn>
              </v-card-actions>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      items:[{
        text: 'Login',
        route: 'dashboardLayout',
      }],

      props: {
        source: String
      }
    };
  }
};
</script>