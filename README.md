Vietnamese (without diacritics - Tiếng Việt không dấu) Analysis Plugin for Elasticsearch 
========================================
Vietnamese (without diacritics) Analysis plugin integrates Vietnamese language without diacritics analysis into Elasticsearch.

The plugin provides the `vi_analyzer` analyzer and `vi_tokenizer` tokenizer. The `vi_analyzer` is composed of the `vi_tokenizer` tokenizer, the lowercase and stop filter.

## Installation on Elasticsearch 6.x

#### In order to install the plugin, choose a version in releases page then run:
```bash
bin/elasticsearch-plugin install link/to/binary/version
```
#### Or to build from source, you need to build it with Maven: [![Build Status](https://travis-ci.org/dwyl/learn-travis.svg?branch=master)](https://github.com/yldbk/elasticsearch-analysis-vietnamese-without-diacritics/tree/master/install)
* Step 1: Build the VnTokenizer
```bash
git clone https://github.com/yldbk/vn-nlp-libraries-vietnamese-without-diacritics.git
cd vn-nlp-libraries-vietnamese-without-diacritics/nlp-parent
mvn install
```
* Step 2: Build the plugin
```bash
git clone https://github.com/yldbk/elasticsearch-analysis-vietnamese-without-diacritics.git
cd elasticsearch-analysis-vietnamese-without-diacritics
mvn package -DskipTests
```
* Step 3: Install the plugin
```bash
mvn clean package
bin/elasticsearch-plugin install file:target/releases/elasticsearch-analysis-vietnamese-6.0.0.zip
```

## Compatible Versions
| Vietnamese Analysis Plugin | Elasticsearch |
| -------------------------- | ------------- |
| master                     | 6.0.0         |
| 5.4.1                      | 5.4.1         |
| 5.3.1                      | 5.3.1         |
| 5.2.1                      | 5.2.1         |
| 2.4.1                      | 2.4.1         |
| 2.4.0                      | 2.4.0         |
| 2.3.5                      | 2.3.5         |
| 2.3.4                      | 2.3.4         |
| 2.3.3                      | 2.3.3         |
| 2.3.2                      | 2.3.2         |
| 2.3.1                      | 2.3.1         |
| 2.3.0                      | 2.3.0         |
| 0.2.2                      | 2.2.0         |
| 0.2.1.1                    | 2.1.1         |
| 0.2.1                      | 2.1.0         |
| 0.2                        | 2.0.0         |
| 0.1.7                      | 1.7+          |
| 0.1.6                      | 1.6+          |
| 0.1.5                      | 1.5+          |
| 0.1.1                      | 1.4+          |
| 0.1                        | 1.3           |

## Thanks to
- [Lê Hồng Phương](http://mim.hus.vnu.edu.vn/phuonglh/) for his VnTokenizer library
- [JetBrains](https://www.jetbrains.com) has provided a free license for their great tool: [IntelliJ IDEA](https://www.jetbrains.com/idea/)

## User guide

The plugin includes the `vi_analyzer` analyzer and `vi_tokenizer` tokenizer.

The `vi_analyzer` is built using the `vi_tokenizer` tokenizer.

 The analyzer analyzes `"Cong nghe thong tin Viet Nam"` `(without diacritics - Tiếng Việt Không dấu)` into `"Cong nghe thong tin"` and `"Viet Nam"` tokens.

License
-------

    This software is licensed under the Apache 2 license, quoted below.

    Licensed under the Apache License, Version 2.0 (the "License"); you may not
    use this file except in compliance with the License. You may obtain a copy of
    the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
    WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the
    License for the specific language governing permissions and limitations under
    the License.
