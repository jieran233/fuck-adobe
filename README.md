# fuck-adobe

A set of rules for Mihomo

I created a script that compares all Windows executable additions and deletions in `C:\` between two "snapshots". I used it to get a list of all executables added by installing PS

https://github.com/jieran233/execdiff

## Note

- The rules are created for PS only currently
- The rules assume PS 2025 is installed in the default location of `C:\`

## Usage

Add the content of `rules.yaml` to the top of routing rules in mihomo config

### Use as Clash Verge Rev global extend script

use `rules.js`

```javascript
// Define main function (script entry)

/**
 * 配置中的规则"config.rules"是一个数组，通过新旧数组合并来添加
 * @param prependRule 添加的数组
 */
const prependRule = [
  // Add the rules here (in `rules.js`)
  // Document: https://wiki.metacubex.one/en/config/rules/
  // "DOMAIN-SUFFIX,example.com,DIRECT",

];
function main(config) {
  // 把旧规则合并到新规则后面(也可以用其它合并数组的办法)
  let oldrules = config["rules"];
  config["rules"] = prependRule.concat(oldrules);
  return config;
}
```