# 如何使用？

## 1.下载或拷贝address.js文件


## 2.使用

### template:
```
    <el-form :model="form_">
      <el-form-item label="地址:" prop="address" width="100%">
        <el-cascader
          v-model="form_.address"
          :options="areaOptions"
          @change="handleChange($event)"
        ></el-cascader>
      </el-form-item>
    </el-form>
```

### js:

```


<script>
import address from "@/utils/address";
export default {
  name: "formView",
  data() {
    return {
      areaOptions: address,
      form_: {
        address: [],
      },
    };
  },
  methods: {
    handleChange(value) {
      console.log(value);
      console.log(this.form_);
    },
  },
};
</script>

```