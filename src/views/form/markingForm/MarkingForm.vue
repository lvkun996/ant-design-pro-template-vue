<template>
  <a-card :bordered="false">
    <k-form-design title="自定义表单" toolbarsTop :fields="['input', 'textarea', 'select', 'checkbox', 'radio', 'date', 'cascader', 'button']" :showHead="false" @save="handleSave" @submit="handleSubmit">
    </k-form-design>
  </a-card>
</template>

<script>
export default {
  data() {
    return {
      jsonData: {
        list: [
          {
            type: 'input',
            icon: 'icon-input',
            options: {
              width: '100%',
              defaultValue: '',
              required: false,
              dataType: 'string',
              pattern: '',
              placeholder: '',
              customClass: '',
              disabled: false,
              labelWidth: 100,
              isLabelWidth: false,
              hidden: false,
              dataBind: true,
              showPassword: false,
              remoteFunc: 'func_1580735211034',
              remoteOption: 'option_1580735211034',
            },
            name: '单行文本',
            key: '1580735211034',
            model: 'input_1580735211034',
            rules: [{ type: 'string', message: '单行文本格式不正确' }],
          },
          {
            type: 'textarea',
            icon: 'icon-diy-com-textarea',
            options: {
              width: '100%',
              defaultValue: '',
              required: false,
              disabled: false,
              pattern: '',
              placeholder: '',
              customClass: '',
              labelWidth: 100,
              isLabelWidth: false,
              hidden: false,
              dataBind: true,
              remoteFunc: 'func_1580735214742',
              remoteOption: 'option_1580735214742',
            },
            name: '多行文本',
            key: '1580735214742',
            model: 'textarea_1580735214742',
            rules: [],
          },
          {
            type: 'radio',
            icon: 'icon-radio-active',
            options: {
              inline: false,
              defaultValue: '',
              showLabel: false,
              options: [
                { value: 'Option 1', label: 'Option 1' },
                { value: 'Option 2', label: 'Option 2' },
                { value: 'Option 3', label: 'Option 3' },
              ],
              required: false,
              width: '',
              remote: false,
              remoteType: 'option',
              remoteOption: 'option_1580735218112',
              remoteOptions: [],
              props: { value: 'value', label: 'label' },
              remoteFunc: 'func_1580735218112',
              customClass: '',
              labelWidth: 100,
              isLabelWidth: false,
              hidden: false,
              dataBind: true,
              disabled: false,
            },
            name: '单选框组',
            key: '1580735218112',
            model: 'radio_1580735218112',
            rules: [],
          },
          {
            type: 'checkbox',
            icon: 'icon-check-box',
            options: {
              inline: false,
              defaultValue: [],
              showLabel: false,
              options: [{ value: 'Option 1' }, { value: 'Option 2' }, { value: 'Option 3' }],
              required: false,
              width: '',
              remote: false,
              remoteType: 'option',
              remoteOption: 'option_1580735222992',
              remoteOptions: [],
              props: { value: 'value', label: 'label' },
              remoteFunc: 'func_1580735222992',
              customClass: '',
              labelWidth: 100,
              isLabelWidth: false,
              hidden: false,
              dataBind: true,
              disabled: false,
            },
            name: '多选框组',
            key: '1580735222992',
            model: 'checkbox_1580735222992',
            rules: [],
          }
        ],
        config: {
          labelWidth: 100,
          labelPosition: 'right',
          size: 'small',
          customClass: '',
          ui: 'element',
          layout: 'horizontal',
          labelCol: 3,
        },
      },
    }
  },
  created() {},
  mounted() {},
  methods: {
    handleSubmit() {
      this.$refs.generateForm
        .getData()
        .then((data) => {
          alert(JSON.stringify(data))
        })
        .catch((e) => {})
    },
    handleSave(values) {
      alert("触发保存方法");
      console.log(values);
    }
  },
}
</script>

<style lang="less" scoped>
</style>
