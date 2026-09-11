# Linter 规则参考总表（236 条）

> - 数据来源：仓库内 `src/data/linter_rules.json`，按各规则的 `sinceDartSdk` 字段筛选（不含 `removed` 状态规则）
> - 每条规则的官方文档：`https://dart.dev/tools/linter-rules/<规则名>`，见末列链接
> - 规则状态：稳定 221 条　🧪 实验性 9 条　💤 已废弃 6 条
> - ⚠️ 标记表示该规则需要较高 SDK 版本，或与同列表中其他规则互相冲突，启用前请确认

| # | 规则 | 说明 | 备注 | 文档 |
| ---: | --- | --- | --- | :---: |
| 1 | `always_declare_return_types` | 显式声明方法的返回类型。 |  | [文档](https://dart.dev/tools/linter-rules/always_declare_return_types) |
| 2 | `always_put_control_body_on_new_line` | 控制结构的语句体始终另起一行书写。 |  | [文档](https://dart.dev/tools/linter-rules/always_put_control_body_on_new_line) |
| 3 | `always_put_required_named_parameters_first` | 将 required 命名参数放在参数列表最前面。 |  | [文档](https://dart.dev/tools/linter-rules/always_put_required_named_parameters_first) |
| 4 | `always_specify_types` | 显式书写类型注解。 | ⚠️ 与同列表的 `omit_local_variable_types`、`omit_obvious_local_variable_types`、`omit_obvious_property_types`、`avoid_types_on_closure_parameters` 冲突 | [文档](https://dart.dev/tools/linter-rules/always_specify_types) |
| 5 | `always_use_package_imports` | 引入 `lib/` 下的文件时使用 `package:` 导入，避免相对导入。 | ⚠️ 与同列表的 `prefer_relative_imports` 互斥，需二选一 | [文档](https://dart.dev/tools/linter-rules/always_use_package_imports) |
| 6 | `annotate_overrides` | 重写父类成员时添加 `@override` 注解。 |  | [文档](https://dart.dev/tools/linter-rules/annotate_overrides) |
| 7 | `annotate_redeclares` | 对重声明（redeclare）的成员添加 `@redeclare` 注解。 | 🧪 实验性规则，可能变更 | [文档](https://dart.dev/tools/linter-rules/annotate_redeclares) |
| 8 | `avoid_annotating_with_dynamic` | 非必要时不要显式标注 `dynamic`。 |  | [文档](https://dart.dev/tools/linter-rules/avoid_annotating_with_dynamic) |
| 9 | `avoid_bool_literals_in_conditional_expressions` | 条件表达式中避免直接出现 bool 字面量。 |  | [文档](https://dart.dev/tools/linter-rules/avoid_bool_literals_in_conditional_expressions) |
| 10 | `avoid_catches_without_on_clauses` | 避免使用不带 `on` 子句的 `catch`。 |  | [文档](https://dart.dev/tools/linter-rules/avoid_catches_without_on_clauses) |
| 11 | `avoid_catching_errors` | 不要显式捕获 `Error` 或实现了它的类型。 |  | [文档](https://dart.dev/tools/linter-rules/avoid_catching_errors) |
| 12 | `avoid_classes_with_only_static_members` | 避免定义只包含静态成员的类。 |  | [文档](https://dart.dev/tools/linter-rules/avoid_classes_with_only_static_members) |
| 13 | `avoid_double_and_int_checks` | 避免对 `double` 和 `int` 做重复的类型检查。 |  | [文档](https://dart.dev/tools/linter-rules/avoid_double_and_int_checks) |
| 14 | `avoid_dynamic_calls` | 避免对 `dynamic` 目标进行方法调用或属性访问。 |  | [文档](https://dart.dev/tools/linter-rules/avoid_dynamic_calls) |
| 15 | `avoid_empty_else` | 避免空的 else 语句。 |  | [文档](https://dart.dev/tools/linter-rules/avoid_empty_else) |
| 16 | `avoid_equals_and_hash_code_on_mutable_classes` | 未标记 `@immutable` 的可变类上避免重写 `==` 和 `hashCode`。 |  | [文档](https://dart.dev/tools/linter-rules/avoid_equals_and_hash_code_on_mutable_classes) |
| 17 | `avoid_escaping_inner_quotes` | 通过改换外层引号，避免对内层引号做转义。 |  | [文档](https://dart.dev/tools/linter-rules/avoid_escaping_inner_quotes) |
| 18 | `avoid_field_initializers_in_const_classes` | const 构造的类中避免使用字段初始化器。 |  | [文档](https://dart.dev/tools/linter-rules/avoid_field_initializers_in_const_classes) |
| 19 | `avoid_final_parameters` | 参数声明避免使用 `final`。 | ⚠️ 与同列表的 `prefer_final_parameters` 互斥，需二选一 | [文档](https://dart.dev/tools/linter-rules/avoid_final_parameters) |
| 20 | `avoid_function_literals_in_foreach_calls` | 避免在 `forEach` 中使用函数字面量（闭包）。 |  | [文档](https://dart.dev/tools/linter-rules/avoid_function_literals_in_foreach_calls) |
| 21 | `avoid_futureor_void` | 避免使用 `FutureOr<void>` 作为返回结果类型。 | 🧪 实验性规则，可能变更 | [文档](https://dart.dev/tools/linter-rules/avoid_futureor_void) |
| 22 | `avoid_implementing_value_types` | 不要去实现重写了 `==` 的值类型类。 |  | [文档](https://dart.dev/tools/linter-rules/avoid_implementing_value_types) |
| 23 | `avoid_init_to_null` | 不要显式将变量初始化为 `null`。 |  | [文档](https://dart.dev/tools/linter-rules/avoid_init_to_null) |
| 24 | `avoid_js_rounded_ints` | 避免使用在 JavaScript 上会因精度问题被舍入的整数。 |  | [文档](https://dart.dev/tools/linter-rules/avoid_js_rounded_ints) |
| 25 | `avoid_multiple_declarations_per_line` | 不要在同一行声明多个变量。 |  | [文档](https://dart.dev/tools/linter-rules/avoid_multiple_declarations_per_line) |
| 26 | `avoid_null_checks_in_equality_operators` | 自定义 `==` 运算符时不要做 `null` 检查。 | 💤 官方已废弃，不建议在新项目中启用 | [文档](https://dart.dev/tools/linter-rules/avoid_null_checks_in_equality_operators) |
| 27 | `avoid_positional_boolean_parameters` | 避免使用位置布尔参数。 |  | [文档](https://dart.dev/tools/linter-rules/avoid_positional_boolean_parameters) |
| 28 | `avoid_print` | 生产代码中避免调用 `print`。 |  | [文档](https://dart.dev/tools/linter-rules/avoid_print) |
| 29 | `avoid_private_typedef_functions` | 避免私有的 typedef 函数类型。 | 💤 官方已废弃，不建议在新项目中启用 | [文档](https://dart.dev/tools/linter-rules/avoid_private_typedef_functions) |
| 30 | `avoid_redundant_argument_values` | 避免传入与默认值相同的冗余参数。 |  | [文档](https://dart.dev/tools/linter-rules/avoid_redundant_argument_values) |
| 31 | `avoid_relative_lib_imports` | 避免以相对路径导入 `lib/` 中的文件。 |  | [文档](https://dart.dev/tools/linter-rules/avoid_relative_lib_imports) |
| 32 | `avoid_renaming_method_parameters` | 重写方法时不要修改参数名称。 |  | [文档](https://dart.dev/tools/linter-rules/avoid_renaming_method_parameters) |
| 33 | `avoid_return_types_on_setters` | setter 不要书写返回类型。 |  | [文档](https://dart.dev/tools/linter-rules/avoid_return_types_on_setters) |
| 34 | `avoid_returning_null_for_void` | 返回类型为 `void` 时避免返回 `null`。 |  | [文档](https://dart.dev/tools/linter-rules/avoid_returning_null_for_void) |
| 35 | `avoid_returning_this` | 避免仅为支持链式调用而在方法中返回 `this`。 |  | [文档](https://dart.dev/tools/linter-rules/avoid_returning_this) |
| 36 | `avoid_setters_without_getters` | 避免只有 setter 而没有 getter。 |  | [文档](https://dart.dev/tools/linter-rules/avoid_setters_without_getters) |
| 37 | `avoid_shadowing_type_parameters` | 避免遮蔽（shadow）类型参数。 |  | [文档](https://dart.dev/tools/linter-rules/avoid_shadowing_type_parameters) |
| 38 | `avoid_single_cascade_in_expression_statements` | 表达式语句中避免只使用单个级联。 |  | [文档](https://dart.dev/tools/linter-rules/avoid_single_cascade_in_expression_statements) |
| 39 | `avoid_slow_async_io` | 避免使用性能较差的异步 `dart:io` 方法。 |  | [文档](https://dart.dev/tools/linter-rules/avoid_slow_async_io) |
| 40 | `avoid_type_to_string` | 生产代码中避免对 `Type` 调用 `toString()`（产物压缩后结果可能变化）。 |  | [文档](https://dart.dev/tools/linter-rules/avoid_type_to_string) |
| 41 | `avoid_types_as_parameter_names` | 避免用类型名作为参数名。 |  | [文档](https://dart.dev/tools/linter-rules/avoid_types_as_parameter_names) |
| 42 | `avoid_types_on_closure_parameters` | 避免为闭包参数标注类型。 | ⚠️ 与同列表的 `always_specify_types` 冲突 | [文档](https://dart.dev/tools/linter-rules/avoid_types_on_closure_parameters) |
| 43 | `avoid_unnecessary_containers` | 避免使用不必要的 `Container`。 |  | [文档](https://dart.dev/tools/linter-rules/avoid_unnecessary_containers) |
| 44 | `avoid_unused_constructor_parameters` | 构造函数中避免定义未使用的参数。 |  | [文档](https://dart.dev/tools/linter-rules/avoid_unused_constructor_parameters) |
| 45 | `avoid_void_async` | 避免返回 `void` 的 `async` 函数。 |  | [文档](https://dart.dev/tools/linter-rules/avoid_void_async) |
| 46 | `avoid_web_libraries_in_flutter` | 除 Flutter Web 插件包外，避免使用仅支持 Web 的库。 |  | [文档](https://dart.dev/tools/linter-rules/avoid_web_libraries_in_flutter) |
| 47 | `await_only_futures` | 只应对 Future 使用 `await`。 |  | [文档](https://dart.dev/tools/linter-rules/await_only_futures) |
| 48 | `camel_case_extensions` | 扩展命名使用 UpperCamelCase。 |  | [文档](https://dart.dev/tools/linter-rules/camel_case_extensions) |
| 49 | `camel_case_types` | 类型命名使用 UpperCamelCase。 |  | [文档](https://dart.dev/tools/linter-rules/camel_case_types) |
| 50 | `cancel_subscriptions` | 及时取消 `dart:async` 的 `StreamSubscription`。 |  | [文档](https://dart.dev/tools/linter-rules/cancel_subscriptions) |
| 51 | `cascade_invocations` | 对同一对象的连续方法调用使用级联（`..`）语法。 |  | [文档](https://dart.dev/tools/linter-rules/cascade_invocations) |
| 52 | `cast_nullable_to_non_nullable` | 不要将可空类型强转为非空类型。 |  | [文档](https://dart.dev/tools/linter-rules/cast_nullable_to_non_nullable) |
| 53 | `close_sinks` | 及时关闭 `dart:core` 的 `Sink`。 |  | [文档](https://dart.dev/tools/linter-rules/close_sinks) |
| 54 | `collection_methods_unrelated_type` | 调用集合方法时传入了不相关类型的参数。 |  | [文档](https://dart.dev/tools/linter-rules/collection_methods_unrelated_type) |
| 55 | `combinators_ordering` | `show`/`hide` 组合子名称按字母顺序排列。 |  | [文档](https://dart.dev/tools/linter-rules/combinators_ordering) |
| 56 | `comment_references` | 文档注释中只引用作用域内的标识符。 |  | [文档](https://dart.dev/tools/linter-rules/comment_references) |
| 57 | `conditional_uri_does_not_exist` | 条件导入（conditional import）指向的 URI 必须存在。 |  | [文档](https://dart.dev/tools/linter-rules/conditional_uri_does_not_exist) |
| 58 | `constant_identifier_names` | 常量标识符使用 lowerCamelCase 命名。 |  | [文档](https://dart.dev/tools/linter-rules/constant_identifier_names) |
| 59 | `control_flow_in_finally` | `finally` 块中避免使用控制流语句。 |  | [文档](https://dart.dev/tools/linter-rules/control_flow_in_finally) |
| 60 | `curly_braces_in_flow_control_structures` | 所有流程控制结构都使用花括号。 |  | [文档](https://dart.dev/tools/linter-rules/curly_braces_in_flow_control_structures) |
| 61 | `dangling_library_doc_comments` | 库级文档注释必须依附在 `library` 指令上。 |  | [文档](https://dart.dev/tools/linter-rules/dangling_library_doc_comments) |
| 62 | `depend_on_referenced_packages` | 引用了其他包就必须在 pubspec 中声明依赖。 |  | [文档](https://dart.dev/tools/linter-rules/depend_on_referenced_packages) |
| 63 | `deprecated_consistency` | 废弃（`@Deprecated`）标注要保持完整一致。 |  | [文档](https://dart.dev/tools/linter-rules/deprecated_consistency) |
| 64 | `deprecated_member_use_from_same_package` | 包内部避免使用本包已标记为废弃的成员。 |  | [文档](https://dart.dev/tools/linter-rules/deprecated_member_use_from_same_package) |
| 65 | `diagnostic_describe_all_properties` | debug 诊断方法中应列出全部公开属性。 |  | [文档](https://dart.dev/tools/linter-rules/diagnostic_describe_all_properties) |
| 66 | `directives_ordering` | 导入与指令排序遵循 Effective Dart 规范。 |  | [文档](https://dart.dev/tools/linter-rules/directives_ordering) |
| 67 | `discarded_futures` | 同步函数中不应丢弃返回 `Future` 的调用，应将其赋值或返回。 |  | [文档](https://dart.dev/tools/linter-rules/discarded_futures) |
| 68 | `do_not_use_environment` | 不要使用编译期环境变量（`String.fromEnvironment` 等）。 |  | [文档](https://dart.dev/tools/linter-rules/do_not_use_environment) |
| 69 | `document_ignores` | 为 `ignore` 注释写明忽略原因。 |  | [文档](https://dart.dev/tools/linter-rules/document_ignores) |
| 70 | `empty_catches` | 避免空的 catch 块。 |  | [文档](https://dart.dev/tools/linter-rules/empty_catches) |
| 71 | `empty_constructor_bodies` | 空构造函数体用 `;` 而非 `{}`。 |  | [文档](https://dart.dev/tools/linter-rules/empty_constructor_bodies) |
| 72 | `empty_statements` | 避免空语句。 |  | [文档](https://dart.dev/tools/linter-rules/empty_statements) |
| 73 | `eol_at_end_of_file` | 文件末尾保留且仅保留一个换行符。 |  | [文档](https://dart.dev/tools/linter-rules/eol_at_end_of_file) |
| 74 | `exhaustive_cases` | 类枚举类中应为所有常量定义 case 分支。 |  | [文档](https://dart.dev/tools/linter-rules/exhaustive_cases) |
| 75 | `file_names` | 源文件命名使用 `lowercase_with_underscores`。 |  | [文档](https://dart.dev/tools/linter-rules/file_names) |
| 76 | `flutter_style_todos` | 使用 Flutter 风格的 TODO 格式：`// TODO(username): message, https://URL`。 |  | [文档](https://dart.dev/tools/linter-rules/flutter_style_todos) |
| 77 | `hash_and_equals` | 重写 `==` 时必须同时重写 `hashCode`。 |  | [文档](https://dart.dev/tools/linter-rules/hash_and_equals) |
| 78 | `implementation_imports` | 不要导入其他包的内部实现文件。 |  | [文档](https://dart.dev/tools/linter-rules/implementation_imports) |
| 79 | `implicit_call_tearoffs` | 将对象当作函数使用时，显式 tear-off 其 `call` 方法。 |  | [文档](https://dart.dev/tools/linter-rules/implicit_call_tearoffs) |
| 80 | `implicit_reopen` | 不要隐式重新开放（reopen）类。 | 🧪 实验性规则，可能变更 | [文档](https://dart.dev/tools/linter-rules/implicit_reopen) |
| 81 | `invalid_case_patterns` | 使用 Dart 3.0 中合法的 case 表达式/模式。 | 🧪 实验性规则，可能变更 | [文档](https://dart.dev/tools/linter-rules/invalid_case_patterns) |
| 82 | `invalid_runtime_check_with_js_interop_types` | 避免对 JS interop 类型做跨平台结果可能不一致的运行时类型检查。 |  | [文档](https://dart.dev/tools/linter-rules/invalid_runtime_check_with_js_interop_types) |
| 83 | `join_return_with_assignment` | 在可行时将 return 语句与赋值合并。 |  | [文档](https://dart.dev/tools/linter-rules/join_return_with_assignment) |
| 84 | `leading_newlines_in_multiline_strings` | 多行字符串以一个换行符开头。 |  | [文档](https://dart.dev/tools/linter-rules/leading_newlines_in_multiline_strings) |
| 85 | `library_annotations` | 库级注解必须依附在 `library` 指令上。 |  | [文档](https://dart.dev/tools/linter-rules/library_annotations) |
| 86 | `library_names` | 库名使用 `lowercase_with_underscores` 风格。 |  | [文档](https://dart.dev/tools/linter-rules/library_names) |
| 87 | `library_prefixes` | 库前缀命名使用 `lowercase_with_underscores`。 |  | [文档](https://dart.dev/tools/linter-rules/library_prefixes) |
| 88 | `library_private_types_in_public_api` | 公开 API 中避免使用私有类型。 |  | [文档](https://dart.dev/tools/linter-rules/library_private_types_in_public_api) |
| 89 | `lines_longer_than_80_chars` | 单行不要超过 80 个字符。 |  | [文档](https://dart.dev/tools/linter-rules/lines_longer_than_80_chars) |
| 90 | `literal_only_boolean_expressions` | 避免仅由字面量组成的布尔表达式。 |  | [文档](https://dart.dev/tools/linter-rules/literal_only_boolean_expressions) |
| 91 | `matching_super_parameters` | 使用与父类构造函数相匹配的 super 参数名。 |  | [文档](https://dart.dev/tools/linter-rules/matching_super_parameters) |
| 92 | `missing_code_block_language_in_doc_comment` | 文档注释中的代码块需要标明语言。 |  | [文档](https://dart.dev/tools/linter-rules/missing_code_block_language_in_doc_comment) |
| 93 | `missing_whitespace_between_adjacent_strings` | 相邻字符串之间缺少空格。 |  | [文档](https://dart.dev/tools/linter-rules/missing_whitespace_between_adjacent_strings) |
| 94 | `no_adjacent_strings_in_list` | 列表中不要使用相邻字符串自动拼接。 |  | [文档](https://dart.dev/tools/linter-rules/no_adjacent_strings_in_list) |
| 95 | `no_default_cases` | switch 中不要写 default（应穷举所有情况）。 | 🧪 实验性规则，可能变更 | [文档](https://dart.dev/tools/linter-rules/no_default_cases) |
| 96 | `no_duplicate_case_values` | switch 中不要出现重复的 case 值。 |  | [文档](https://dart.dev/tools/linter-rules/no_duplicate_case_values) |
| 97 | `no_leading_underscores_for_library_prefixes` | 库前缀避免以下划线开头。 |  | [文档](https://dart.dev/tools/linter-rules/no_leading_underscores_for_library_prefixes) |
| 98 | `no_leading_underscores_for_local_identifiers` | 局部标识符避免以下划线开头。 |  | [文档](https://dart.dev/tools/linter-rules/no_leading_underscores_for_local_identifiers) |
| 99 | `no_literal_bool_comparisons` | 不要将布尔表达式与 bool 字面量直接比较。 |  | [文档](https://dart.dev/tools/linter-rules/no_literal_bool_comparisons) |
| 100 | `no_logic_in_create_state` | 不要在 `createState` 中放置业务逻辑。 |  | [文档](https://dart.dev/tools/linter-rules/no_logic_in_create_state) |
| 101 | `no_runtimetype_tostring` | 避免对 `runtimeType` 调用 `toString()`。 |  | [文档](https://dart.dev/tools/linter-rules/no_runtimetype_tostring) |
| 102 | `no_self_assignments` | 不要把变量赋值给它自身。 |  | [文档](https://dart.dev/tools/linter-rules/no_self_assignments) |
| 103 | `no_wildcard_variable_uses` | 不要使用通配符参数或变量。 |  | [文档](https://dart.dev/tools/linter-rules/no_wildcard_variable_uses) |
| 104 | `non_constant_identifier_names` | 非常量标识符使用 lowerCamelCase 命名。 |  | [文档](https://dart.dev/tools/linter-rules/non_constant_identifier_names) |
| 105 | `noop_primitive_operations` | 避免没有实际作用的基础类型操作。 |  | [文档](https://dart.dev/tools/linter-rules/noop_primitive_operations) |
| 106 | `null_check_on_nullable_type_parameter` | 不要对可能为可空的类型参数做 null 检查。 |  | [文档](https://dart.dev/tools/linter-rules/null_check_on_nullable_type_parameter) |
| 107 | `null_closures` | 需要闭包的参数不要传入 `null`。 |  | [文档](https://dart.dev/tools/linter-rules/null_closures) |
| 108 | `omit_local_variable_types` | 局部变量可省略类型注解。 | ⚠️ 与同列表的 `always_specify_types` 互斥 | [文档](https://dart.dev/tools/linter-rules/omit_local_variable_types) |
| 109 | `omit_obvious_local_variable_types` | 局部变量应省略显而易见的类型注解。 | ⚠️ 与同列表的 `always_specify_types` 冲突 | [文档](https://dart.dev/tools/linter-rules/omit_obvious_local_variable_types) |
| 110 | `omit_obvious_property_types` | 顶层变量与静态变量应省略显而易见的类型注解。 | ⚠️ 与同列表的 `always_specify_types` 冲突 | [文档](https://dart.dev/tools/linter-rules/omit_obvious_property_types) |
| 111 | `one_member_abstracts` | 只有一个成员的抽象类可直接用函数替代。 | 💤 官方已废弃，不建议在新项目中启用 | [文档](https://dart.dev/tools/linter-rules/one_member_abstracts) |
| 112 | `only_throw_errors` | 只抛出 `Exception` 或 `Error` 子类的实例。 |  | [文档](https://dart.dev/tools/linter-rules/only_throw_errors) |
| 113 | `overridden_fields` | 不要重写字段。 |  | [文档](https://dart.dev/tools/linter-rules/overridden_fields) |
| 114 | `package_names` | 包名使用 `lowercase_with_underscores`。 |  | [文档](https://dart.dev/tools/linter-rules/package_names) |
| 115 | `package_prefixed_library_names` | 库名以包名加点分路径作为前缀。 |  | [文档](https://dart.dev/tools/linter-rules/package_prefixed_library_names) |
| 116 | `parameter_assignments` | 不要对函数或方法的参数重新赋值。 |  | [文档](https://dart.dev/tools/linter-rules/parameter_assignments) |
| 117 | `prefer_adjacent_string_concatenation` | 使用相邻字符串形式拼接字符串字面量。 |  | [文档](https://dart.dev/tools/linter-rules/prefer_adjacent_string_concatenation) |
| 118 | `prefer_asserts_in_initializer_lists` | 断言优先放在构造函数的初始化列表中。 |  | [文档](https://dart.dev/tools/linter-rules/prefer_asserts_in_initializer_lists) |
| 119 | `prefer_asserts_with_message` | 断言建议附带说明信息。 |  | [文档](https://dart.dev/tools/linter-rules/prefer_asserts_with_message) |
| 120 | `prefer_collection_literals` | 尽可能使用集合字面量。 |  | [文档](https://dart.dev/tools/linter-rules/prefer_collection_literals) |
| 121 | `prefer_conditional_assignment` | 优先使用 `??=`，而非判空后赋值。 |  | [文档](https://dart.dev/tools/linter-rules/prefer_conditional_assignment) |
| 122 | `prefer_const_constructors` | 对常量构造函数优先使用 `const`。 |  | [文档](https://dart.dev/tools/linter-rules/prefer_const_constructors) |
| 123 | `prefer_const_constructors_in_immutables` | `@immutable` 类优先声明 const 构造函数。 |  | [文档](https://dart.dev/tools/linter-rules/prefer_const_constructors_in_immutables) |
| 124 | `prefer_const_declarations` | 常量声明优先使用 `const` 而非 `final`。 |  | [文档](https://dart.dev/tools/linter-rules/prefer_const_declarations) |
| 125 | `prefer_const_literals_to_create_immutables` | 传给 `@immutable` 类的字面量参数优先使用 const。 |  | [文档](https://dart.dev/tools/linter-rules/prefer_const_literals_to_create_immutables) |
| 126 | `prefer_constructors_over_static_methods` | 创建实例优先使用构造函数而非静态方法。 |  | [文档](https://dart.dev/tools/linter-rules/prefer_constructors_over_static_methods) |
| 127 | `prefer_contains` | 使用 `contains` 判断 `List`/`String` 的包含关系。 |  | [文档](https://dart.dev/tools/linter-rules/prefer_contains) |
| 128 | `prefer_double_quotes` | 在不需要转义时优先使用双引号。 | ⚠️ 与同列表的 `prefer_single_quotes` 互斥，需二选一 | [文档](https://dart.dev/tools/linter-rules/prefer_double_quotes) |
| 129 | `prefer_expression_function_bodies` | 仅含单个 return 的简短成员优先使用 `=>` 函数体。 |  | [文档](https://dart.dev/tools/linter-rules/prefer_expression_function_bodies) |
| 130 | `prefer_final_fields` | 不会变化的私有字段应声明为 `final`。 |  | [文档](https://dart.dev/tools/linter-rules/prefer_final_fields) |
| 131 | `prefer_final_in_for_each` | for-each 循环变量未被重新赋值时使用 `final`。 | ⚠️ 与同列表的 `unnecessary_final` 互斥 | [文档](https://dart.dev/tools/linter-rules/prefer_final_in_for_each) |
| 132 | `prefer_final_locals` | 局部变量未被重新赋值时使用 `final`。 | ⚠️ 与同列表的 `unnecessary_final` 互斥 | [文档](https://dart.dev/tools/linter-rules/prefer_final_locals) |
| 133 | `prefer_final_parameters` | 参数未被重新赋值时使用 `final`。 | 💤 官方已废弃，不建议在新项目中启用<br>⚠️ 与同列表的 `avoid_final_parameters` 互斥，需二选一 | [文档](https://dart.dev/tools/linter-rules/prefer_final_parameters) |
| 134 | `prefer_for_elements_to_map_fromIterable` | 从 Iterable 构建 Map 时优先使用 for 元素。 |  | [文档](https://dart.dev/tools/linter-rules/prefer_for_elements_to_map_fromIterable) |
| 135 | `prefer_foreach` | 仅需对所有元素执行操作时使用 `forEach`。 | ⚠️ 与同列表的 `avoid_function_literals_in_foreach_calls` 同时启用时，仅 tear-off 形式可用 `forEach` | [文档](https://dart.dev/tools/linter-rules/prefer_foreach) |
| 136 | `prefer_function_declarations_over_variables` | 将函数绑定到名称时使用函数声明。 |  | [文档](https://dart.dev/tools/linter-rules/prefer_function_declarations_over_variables) |
| 137 | `prefer_generic_function_type_aliases` | 优先使用泛型函数类型别名（新式 typedef 语法）。 |  | [文档](https://dart.dev/tools/linter-rules/prefer_generic_function_type_aliases) |
| 138 | `prefer_if_elements_to_conditional_expressions` | 集合中优先使用 if 元素而非条件表达式。 |  | [文档](https://dart.dev/tools/linter-rules/prefer_if_elements_to_conditional_expressions) |
| 139 | `prefer_if_null_operators` | 优先使用 `??` 运算符。 |  | [文档](https://dart.dev/tools/linter-rules/prefer_if_null_operators) |
| 140 | `prefer_initializing_formals` | 尽可能使用初始化形参（`this.x`）。 |  | [文档](https://dart.dev/tools/linter-rules/prefer_initializing_formals) |
| 141 | `prefer_inlined_adds` | 尽可能内联声明列表元素（collection-if/for）。 |  | [文档](https://dart.dev/tools/linter-rules/prefer_inlined_adds) |
| 142 | `prefer_int_literals` | 优先使用 int 字面量而非 double 字面量。 |  | [文档](https://dart.dev/tools/linter-rules/prefer_int_literals) |
| 143 | `prefer_interpolation_to_compose_strings` | 使用字符串插值来拼接字符串。 |  | [文档](https://dart.dev/tools/linter-rules/prefer_interpolation_to_compose_strings) |
| 144 | `prefer_is_empty` | 对 `Iterable` 和 `Map` 使用 `isEmpty`。 |  | [文档](https://dart.dev/tools/linter-rules/prefer_is_empty) |
| 145 | `prefer_is_not_empty` | 使用 `isNotEmpty`。 |  | [文档](https://dart.dev/tools/linter-rules/prefer_is_not_empty) |
| 146 | `prefer_is_not_operator` | 优先使用 `is!` 运算符。 |  | [文档](https://dart.dev/tools/linter-rules/prefer_is_not_operator) |
| 147 | `prefer_iterable_whereType` | 对可迭代对象优先使用 `whereType` 做类型过滤。 |  | [文档](https://dart.dev/tools/linter-rules/prefer_iterable_whereType) |
| 148 | `prefer_mixin` | 优先使用 mixin。 |  | [文档](https://dart.dev/tools/linter-rules/prefer_mixin) |
| 149 | `prefer_null_aware_method_calls` | 优先使用空感知方法调用（`?.`）。 |  | [文档](https://dart.dev/tools/linter-rules/prefer_null_aware_method_calls) |
| 150 | `prefer_null_aware_operators` | 优先使用空感知运算符。 |  | [文档](https://dart.dev/tools/linter-rules/prefer_null_aware_operators) |
| 151 | `prefer_relative_imports` | 引入 `lib/` 内文件时优先使用相对导入。 | ⚠️ 与同列表的 `always_use_package_imports` 互斥，需二选一 | [文档](https://dart.dev/tools/linter-rules/prefer_relative_imports) |
| 152 | `prefer_single_quotes` | 优先使用单引号（仅字符串内含单引号时才用双引号）。 | ⚠️ 与同列表的 `prefer_double_quotes` 互斥，需二选一 | [文档](https://dart.dev/tools/linter-rules/prefer_single_quotes) |
| 153 | `prefer_spread_collections` | 尽可能使用展开（spread）语法构建集合。 |  | [文档](https://dart.dev/tools/linter-rules/prefer_spread_collections) |
| 154 | `prefer_typing_uninitialized_variables` | 未初始化的变量和字段要显式标注类型。 |  | [文档](https://dart.dev/tools/linter-rules/prefer_typing_uninitialized_variables) |
| 155 | `prefer_void_to_null` | 除非确有必要，不要使用 `Null` 类型，应使用 `void`。 |  | [文档](https://dart.dev/tools/linter-rules/prefer_void_to_null) |
| 156 | `provide_deprecation_message` | 通过 `@Deprecated("message")` 提供废弃说明。 |  | [文档](https://dart.dev/tools/linter-rules/provide_deprecation_message) |
| 157 | `public_member_api_docs` | 所有公开成员都应编写文档注释。 |  | [文档](https://dart.dev/tools/linter-rules/public_member_api_docs) |
| 158 | `recursive_getters` | getter 不能递归返回自身。 |  | [文档](https://dart.dev/tools/linter-rules/recursive_getters) |
| 159 | `remove_deprecations_in_breaking_versions` | 应在主版本（major）中移除/处理已废弃的 API。 |  | [文档](https://dart.dev/tools/linter-rules/remove_deprecations_in_breaking_versions) |
| 160 | `require_trailing_commas` | 所有参数列表与实参列表都使用尾随逗号。 |  | [文档](https://dart.dev/tools/linter-rules/require_trailing_commas) |
| 161 | `secure_pubspec_urls` | `pubspec.yaml` 中的 URL 必须使用 https。 |  | [文档](https://dart.dev/tools/linter-rules/secure_pubspec_urls) |
| 162 | `simplify_variable_pattern` | 变量模式中避免多余的成员名。 |  | [文档](https://dart.dev/tools/linter-rules/simplify_variable_pattern) |
| 163 | `sized_box_for_whitespace` | 用 `SizedBox` 来表达留白。 |  | [文档](https://dart.dev/tools/linter-rules/sized_box_for_whitespace) |
| 164 | `sized_box_shrink_expand` | 使用 `SizedBox.shrink` / `SizedBox.expand` 命名构造。 |  | [文档](https://dart.dev/tools/linter-rules/sized_box_shrink_expand) |
| 165 | `slash_for_doc_comments` | 文档注释优先使用 `///`。 |  | [文档](https://dart.dev/tools/linter-rules/slash_for_doc_comments) |
| 166 | `sort_child_properties_last` | 创建 widget 时将 `child` 属性放在最后。 |  | [文档](https://dart.dev/tools/linter-rules/sort_child_properties_last) |
| 167 | `sort_constructors_first` | 构造函数声明排在其他成员之前。 |  | [文档](https://dart.dev/tools/linter-rules/sort_constructors_first) |
| 168 | `sort_pub_dependencies` | pub 依赖按字母顺序排列。 |  | [文档](https://dart.dev/tools/linter-rules/sort_pub_dependencies) |
| 169 | `sort_unnamed_constructors_first` | 未命名构造函数的声明排在最前面。 |  | [文档](https://dart.dev/tools/linter-rules/sort_unnamed_constructors_first) |
| 170 | `specify_nonobvious_local_variable_types` | 局部变量类型不明显时显式标注类型。 |  | [文档](https://dart.dev/tools/linter-rules/specify_nonobvious_local_variable_types) |
| 171 | `specify_nonobvious_property_types` | 顶层变量与静态变量类型不明显时显式标注类型。 |  | [文档](https://dart.dev/tools/linter-rules/specify_nonobvious_property_types) |
| 172 | `strict_top_level_inference` | 顶层声明必须显式标注类型，不允许依赖推断。 |  | [文档](https://dart.dev/tools/linter-rules/strict_top_level_inference) |
| 173 | `switch_on_type` | 避免直接对 `Type` 使用 switch。 |  | [文档](https://dart.dev/tools/linter-rules/switch_on_type) |
| 174 | `test_types_in_equals` | 在 `operator ==(Object other)` 中检查参数类型。 |  | [文档](https://dart.dev/tools/linter-rules/test_types_in_equals) |
| 175 | `throw_in_finally` | 避免在 `finally` 块中抛出异常。 |  | [文档](https://dart.dev/tools/linter-rules/throw_in_finally) |
| 176 | `tighten_type_of_initializing_formals` | 收紧初始化形参（`this.x`）的类型。 |  | [文档](https://dart.dev/tools/linter-rules/tighten_type_of_initializing_formals) |
| 177 | `type_annotate_public_apis` | 公开 API 必须标注类型。 |  | [文档](https://dart.dev/tools/linter-rules/type_annotate_public_apis) |
| 178 | `type_init_formals` | 初始化形参（`this.x`）不要标注类型。 |  | [文档](https://dart.dev/tools/linter-rules/type_init_formals) |
| 179 | `type_literal_in_constant_pattern` | 常量模式中不要使用类型字面量。 |  | [文档](https://dart.dev/tools/linter-rules/type_literal_in_constant_pattern) |
| 180 | `unawaited_futures` | `async` 函数体中的 `Future` 必须被 `await`，或用 `dart:async` 的 `unawaited` 标记。 |  | [文档](https://dart.dev/tools/linter-rules/unawaited_futures) |
| 181 | `unintended_html_in_doc_comment` | 文档注释中的尖括号会被 Markdown 当作 HTML 处理，注意误用。 |  | [文档](https://dart.dev/tools/linter-rules/unintended_html_in_doc_comment) |
| 182 | `unnecessary_async` | 没有 `await` 就不要声明为 `async`。 | 🧪 实验性规则，可能变更 | [文档](https://dart.dev/tools/linter-rules/unnecessary_async) |
| 183 | `unnecessary_await_in_return` | return 中避免多余的 `await`。 | 💤 官方已废弃，不建议在新项目中启用 | [文档](https://dart.dev/tools/linter-rules/unnecessary_await_in_return) |
| 184 | `unnecessary_brace_in_string_interps` | 非必要时字符串插值不要加花括号。 |  | [文档](https://dart.dev/tools/linter-rules/unnecessary_brace_in_string_interps) |
| 185 | `unnecessary_breaks` | 在 break 已被隐含的情况下不要显式书写 `break`。 |  | [文档](https://dart.dev/tools/linter-rules/unnecessary_breaks) |
| 186 | `unnecessary_const` | 避免多余的 `const` 关键字。 |  | [文档](https://dart.dev/tools/linter-rules/unnecessary_const) |
| 187 | `unnecessary_constructor_name` | 避免多余的 `.new` 构造名。 |  | [文档](https://dart.dev/tools/linter-rules/unnecessary_constructor_name) |
| 188 | `unnecessary_final` | 局部变量不要使用 `final`。 | ⚠️ 与同列表的 `prefer_final_locals`、`prefer_final_in_for_each` 互斥 | [文档](https://dart.dev/tools/linter-rules/unnecessary_final) |
| 189 | `unnecessary_getters_setters` | 不要仅为了“保险”而给字段包一层 getter/setter。 |  | [文档](https://dart.dev/tools/linter-rules/unnecessary_getters_setters) |
| 190 | `unnecessary_ignore` | 不要 ignore 实际并不会产生的诊断码。 |  | [文档](https://dart.dev/tools/linter-rules/unnecessary_ignore) |
| 191 | `unnecessary_lambdas` | 能用 tear-off 时不要再包一层闭包（lambda）。 |  | [文档](https://dart.dev/tools/linter-rules/unnecessary_lambdas) |
| 192 | `unnecessary_late` | 不需要时不要写 `late`。 |  | [文档](https://dart.dev/tools/linter-rules/unnecessary_late) |
| 193 | `unnecessary_library_directive` | 没有文档注释或注解时避免多余的 `library` 指令。 |  | [文档](https://dart.dev/tools/linter-rules/unnecessary_library_directive) |
| 194 | `unnecessary_library_name` | `library` 声明中不要指定库名。 |  | [文档](https://dart.dev/tools/linter-rules/unnecessary_library_name) |
| 195 | `unnecessary_new` | 避免多余的 `new` 关键字。 |  | [文档](https://dart.dev/tools/linter-rules/unnecessary_new) |
| 196 | `unnecessary_null_aware_assignments` | 避免无意义的空感知赋值（`??= null`）。 |  | [文档](https://dart.dev/tools/linter-rules/unnecessary_null_aware_assignments) |
| 197 | `unnecessary_null_aware_operator_on_extension_on_nullable` | 可空类型的扩展上存在多余的空感知运算符。 |  | [文档](https://dart.dev/tools/linter-rules/unnecessary_null_aware_operator_on_extension_on_nullable) |
| 198 | `unnecessary_null_checks` | 避免多余的 `null` 检查。 |  | [文档](https://dart.dev/tools/linter-rules/unnecessary_null_checks) |
| 199 | `unnecessary_null_in_if_null_operators` | `??` 运算符中避免显式写 `null`。 |  | [文档](https://dart.dev/tools/linter-rules/unnecessary_null_in_if_null_operators) |
| 200 | `unnecessary_nullable_for_final_variable_declarations` | 以非空值初始化的 final 变量不要声明为可空类型。 |  | [文档](https://dart.dev/tools/linter-rules/unnecessary_nullable_for_final_variable_declarations) |
| 201 | `unnecessary_overrides` | 仅以相同参数调用 super 方法的重写没有意义。 |  | [文档](https://dart.dev/tools/linter-rules/unnecessary_overrides) |
| 202 | `unnecessary_parenthesis` | 移除不必要的括号。 |  | [文档](https://dart.dev/tools/linter-rules/unnecessary_parenthesis) |
| 203 | `unnecessary_raw_strings` | 避免不必要的 raw 字符串。 |  | [文档](https://dart.dev/tools/linter-rules/unnecessary_raw_strings) |
| 204 | `unnecessary_statements` | 避免没有作用的多余语句。 |  | [文档](https://dart.dev/tools/linter-rules/unnecessary_statements) |
| 205 | `unnecessary_string_escapes` | 移除字符串中多余的反斜杠转义。 |  | [文档](https://dart.dev/tools/linter-rules/unnecessary_string_escapes) |
| 206 | `unnecessary_string_interpolations` | 避免不必要的字符串插值。 |  | [文档](https://dart.dev/tools/linter-rules/unnecessary_string_interpolations) |
| 207 | `unnecessary_this` | 除非为避免名称遮蔽，否则访问成员时不要写 `this`。 |  | [文档](https://dart.dev/tools/linter-rules/unnecessary_this) |
| 208 | `unnecessary_to_list_in_spreads` | 展开（spread）中避免多余的 `toList()`。 |  | [文档](https://dart.dev/tools/linter-rules/unnecessary_to_list_in_spreads) |
| 209 | `unnecessary_unawaited` | 避免不必要的 `unawaited`。 |  | [文档](https://dart.dev/tools/linter-rules/unnecessary_unawaited) |
| 210 | `unnecessary_underscores` | 可以移除多余的下划线（通配符）。 |  | [文档](https://dart.dev/tools/linter-rules/unnecessary_underscores) |
| 211 | `unreachable_from_main` | 可执行库中存在从 `main` 不可达的顶层成员。 |  | [文档](https://dart.dev/tools/linter-rules/unreachable_from_main) |
| 212 | `unrelated_type_equality_checks` | 不要对不相关类型的引用做 `==` 比较。 |  | [文档](https://dart.dev/tools/linter-rules/unrelated_type_equality_checks) |
| 213 | `unsafe_variance` | 不安全的类型变化：类型变量出现在非协变位置。 | 🧪 实验性规则，可能变更 | [文档](https://dart.dev/tools/linter-rules/unsafe_variance) |
| 214 | `use_build_context_synchronously` | 不要跨异步间隙（asynchronous gap）使用 `BuildContext`。 |  | [文档](https://dart.dev/tools/linter-rules/use_build_context_synchronously) |
| 215 | `use_colored_box` | 优先使用 `ColoredBox`。 |  | [文档](https://dart.dev/tools/linter-rules/use_colored_box) |
| 216 | `use_decorated_box` | 优先使用 `DecoratedBox`。 |  | [文档](https://dart.dev/tools/linter-rules/use_decorated_box) |
| 217 | `use_enums` | 具备枚举语义时优先使用 enum，而不是模拟枚举的类。 |  | [文档](https://dart.dev/tools/linter-rules/use_enums) |
| 218 | `use_full_hex_values_for_flutter_colors` | 实例化 `Color` 时使用 8 位十六进制值（如 `0xFFFFFFFF`）。 |  | [文档](https://dart.dev/tools/linter-rules/use_full_hex_values_for_flutter_colors) |
| 219 | `use_function_type_syntax_for_parameters` | 参数的函数类型使用泛型函数语法。 |  | [文档](https://dart.dev/tools/linter-rules/use_function_type_syntax_for_parameters) |
| 220 | `use_if_null_to_convert_nulls_to_bools` | 使用 `??` 运算符将 `null` 转换为 `bool`。 | 💤 官方已废弃，不建议在新项目中启用 | [文档](https://dart.dev/tools/linter-rules/use_if_null_to_convert_nulls_to_bools) |
| 221 | `use_is_even_rather_than_modulo` | 判断奇偶优先使用 `isOdd`/`isEven`，而非 `% 2`。 |  | [文档](https://dart.dev/tools/linter-rules/use_is_even_rather_than_modulo) |
| 222 | `use_key_in_widget_constructors` | widget 构造函数应包含 `key` 参数。 |  | [文档](https://dart.dev/tools/linter-rules/use_key_in_widget_constructors) |
| 223 | `use_late_for_private_fields_and_variables` | 非空的私有字段与变量优先使用 `late`。 | 🧪 实验性规则，可能变更 | [文档](https://dart.dev/tools/linter-rules/use_late_for_private_fields_and_variables) |
| 224 | `use_named_constants` | 优先使用预定义的命名常量。 |  | [文档](https://dart.dev/tools/linter-rules/use_named_constants) |
| 225 | `use_null_aware_elements` | 判空的 if 元素可以替换为空感知元素。 |  | [文档](https://dart.dev/tools/linter-rules/use_null_aware_elements) |
| 226 | `use_raw_strings` | 使用 raw 字符串以避免转义。 |  | [文档](https://dart.dev/tools/linter-rules/use_raw_strings) |
| 227 | `use_rethrow_when_possible` | 重新抛出捕获的异常时使用 `rethrow`。 |  | [文档](https://dart.dev/tools/linter-rules/use_rethrow_when_possible) |
| 228 | `use_setters_to_change_properties` | 语义上是修改属性的操作应使用 setter。 |  | [文档](https://dart.dev/tools/linter-rules/use_setters_to_change_properties) |
| 229 | `use_string_buffers` | 循环拼接字符串时使用 `StringBuffer`。 |  | [文档](https://dart.dev/tools/linter-rules/use_string_buffers) |
| 230 | `use_string_in_part_of_directives` | `part of` 指令使用字符串 URI 形式。 |  | [文档](https://dart.dev/tools/linter-rules/use_string_in_part_of_directives) |
| 231 | `use_super_parameters` | 尽可能使用 super 超参数（super-initializer）。 | 🧪 实验性规则，可能变更 | [文档](https://dart.dev/tools/linter-rules/use_super_parameters) |
| 232 | `use_test_throws_matchers` | 使用 `throwsA` 匹配器，而不是 `fail()`。 |  | [文档](https://dart.dev/tools/linter-rules/use_test_throws_matchers) |
| 233 | `use_to_and_as_if_applicable` | 适用时方法名以 `to`/`_to` 或 `as`/`_as` 开头。 |  | [文档](https://dart.dev/tools/linter-rules/use_to_and_as_if_applicable) |
| 234 | `use_truncating_division` | 使用截断除法（`~/`）。 |  | [文档](https://dart.dev/tools/linter-rules/use_truncating_division) |
| 235 | `valid_regexps` | 使用合法的正则表达式语法。 |  | [文档](https://dart.dev/tools/linter-rules/valid_regexps) |
| 236 | `void_checks` | 不要向 `void` 类型的位置赋值。 |  | [文档](https://dart.dev/tools/linter-rules/void_checks) |
