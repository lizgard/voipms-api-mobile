<template>
    <Page>
        <ActionBar title="VoIP.ms API Setting"/>
        <TabView :selectedIndex="selectedIndex" @selectedIndexChange="indexChange" tabTextColor="black" selectedTabTextColor="#a9a9a9" >
            <TabViewItem title="Tab 1">
                <GridLayout columns="*" rows="*">
                    <Label class="message" :text="msg" col="0" row="0"/>
                </GridLayout>
            </TabViewItem>

            <TabViewItem title="Settings">
                <Label text="Content for Tab 2" />
            </TabViewItem>
        </TabView>
    </Page>
</template>

<script lang="ts">
  export default {
    data() {
      return {
        msg: 'El comunismo por el bien de todos'
      }
    },

    methods: {
        indexChange (args): void {
            let newIndex = args.value;
            console.log('Current tab index: ' + newIndex);
            alert('Current tab index: ' + newIndex);
        }
    }
  }
</script>

<style scoped>
    ActionBar {
        background-color: #C3C3C3;
        color: #ffffff;
    }

    .message {
        vertical-align: center;
        text-align: center;
        font-size: 20;
        color: #333333;
    }
</style>
