<template lang="html">
  <div id="buttons" class="">
    <pageHeader :title="info.components.items.buttons.title" :subTitle="info.components.items.buttons.subTitle" :message="info.components.items.buttons.message" />
    <codeMirror>
      <code slot="codeSlot">
        &lt;div class="content__buttons"&gt;
          &lt;ul class="content__buttons__list"&gt;
              &lt;li class="content__buttons__item"&gt;
                  &lt;div class="content__buttons__block"&gt;
                      &lt;asp:Button ID="btnConfirmar" runat="server" Text="Confirmar" CssClass="content__buttons__btn" Visible="true"  OnClick="bntConfirmar_Click"/&gt;
                  &lt;/div&gt;
              &lt;/li&gt;
          &lt;/ul&gt;
        &lt;/div&gt;
      </code>
    </codeMirror>
    <componentInfo :title="info.components.items.buttons.titleInfo" :message="info.components.items.buttons.infoMessage" :listItem="info.components.items.buttons.listInfo"/>
  </div>
</template>

<script>
  import info from '@/static/data/info.json';
  import base from '@/static/data/base.json';
  import pageHeader from '@/components/page-header';
  import codeMirror from '@/components/code-mirror';
  import componentInfo from '@/components/component-info';

  export default {
    components: {
      pageHeader,
      codeMirror,
      componentInfo
    },
    data() {
      return {
        info,
        code: '<div class="content__buttons">\
                            <ul class="content__buttons__list">\
                                <li class="content__buttons__item">\
                                    <div class="content__buttons__block">\
                                        <asp:Button ID="btnConfirmar" runat="server" Text="Confirmar" CssClass="content__buttons__btn" Visible="true"  OnClick="bntConfirmar_Click"/>\
                                    </div>\
                                </li>\
                            </ul>\
                        </div>'
      }
    }
  }
</script>

<style lang="css">
</style>
