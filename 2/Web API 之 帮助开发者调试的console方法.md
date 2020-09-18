# Web API 之 帮助开发者调试的console方法

<img src="../assets/2/console.png" /> 

在`node_modules/@types/node - Definitions`中查看到了`console`定义的`interface`源码，可以自己动手试试哦

## 源码展示

按住`ctrl`键点击`console`方法可查看以下代码:

```js
declare module "console" {
    import { InspectOptions } from 'util';

    global {
        // This needs to be global to avoid TS2403 in case lib.dom.d.ts is present in the same build
        interface Console {
            Console: NodeJS.ConsoleConstructor;
            /**
             * A simple assertion test that verifies whether `value` is truthy.
             * If it is not, an `AssertionError` is thrown.
             * If provided, the error `message` is formatted using `util.format()` and used as the error message.
             * 一个简单的断言测试，用于验证“value”是否真实
             * 如果不是，则抛出“AssertionError”
             * 如果提供了错误“message”，则使用`util.格式（）`并用作错误消息
             */
            assert(value: any, message?: string, ...optionalParams: any[]): void;
            /**
             * When `stdout` is a TTY, calling `console.clear()` will attempt to clear the TTY.
             * When `stdout` is not a TTY, this method does nothing.
             * 清除控制台的打印信息
             */
            clear(): void;
            /**
             * Maintains an internal counter specific to `label` and outputs to `stdout` the number of times `console.count()` has been called with the given `label`.
             * 维护特定于“label”的内部计数器，并将次数输出到“stdout”`控制台.count已使用给定的“label”调用了
             * 可以自动输出每一次执行过的打印结果
             */
            count(label?: string): void;
            /**
             * Resets the internal counter specific to `label`.
             * 重置特定于“label”的内部计数器
             */
            countReset(label?: string): void;
            /**
             * The `console.debug()` function is an alias for {@link console.log()}.
             * 和console.log打印效果一样，但谷歌浏览器不支持console.debug
             */
            debug(message?: any, ...optionalParams: any[]): void;
            /**
             * Uses {@link util.inspect()} on `obj` and prints the resulting string to `stdout`.
             * This function bypasses any custom `inspect()` function defined on `obj`.
             * 可打印Object对象
             */
            dir(obj: any, options?: InspectOptions): void;
            /**
             * This method calls {@link console.log()} passing it the arguments received. Please note that this method does not produce any XML formatting
             * 此方法调用{@link控制台.log（）}将收到的参数传递给它。请注意，此方法不生成任何XML格式
             */
            dirxml(...data: any[]): void;
            /**
             * Prints to `stderr` with newline.
             * 打印信息显示红色的错误图标
             */
            error(message?: any, ...optionalParams: any[]): void;
            /**
             * Increases indentation of subsequent lines by two spaces.
             * If one or more `label`s are provided, those are printed first without the additional indentation.
             * 将后续行的缩进增加两个空格。
             * 如果提供了一个或多个“label”，则首先打印这些标签，而不附加缩进
             */
            group(...label: any[]): void;
            /**
             * The `console.groupCollapsed()` function is an alias for {@link console.group()}.
             * console.group的别名
             */
            groupCollapsed(...label: any[]): void;
            /**
             * Decreases indentation of subsequent lines by two spaces.
             * 将后续行的缩进减少两个空格。
             */
            groupEnd(): void;
            /**
             * The {@link console.info()} function is an alias for {@link console.log()}.
             */
            info(message?: any, ...optionalParams: any[]): void;
            /**
             * Prints to `stdout` with newline.
             * 用换行符打印到“stdout”
             */
            log(message?: any, ...optionalParams: any[]): void;
            /**
             * This method does not display anything unless used in the inspector.
             * Prints to `stdout` the array `array` formatted as a table.
             * 此方法不显示任何内容，除非在检查器中使用。
             * 打印到格式为表的数组array。
             */
            table(tabularData: any, properties?: string[]): void;
            /**
             * Starts a timer that can be used to compute the duration of an operation. Timers are identified by a unique `label`.
             * 启动可用于计算操作持续时间的计时器。计时器由唯一的“label”标识
             */
            time(label?: string): void;
            /**
             * Stops a timer that was previously started by calling {@link console.time()} and prints the result to `stdout`.
             * 计算console.time行开始到timeEnd行代码运行的时间
             */
            timeEnd(label?: string): void;
            /**
             * For a timer that was previously started by calling {@link console.time()}, prints the elapsed time and other `data` arguments to `stdout`.
             * 对于以前通过调用{@link console.time（）}，将运行时间和其他“data”参数打印到“stdout”。
             */
            timeLog(label?: string, ...data: any[]): void;
            /**
             * Prints to `stderr` the string 'Trace :', followed by the {@link util.format()} formatted message and stack trace to the current position in the code.
             * 打印到“stderr”字符串“Trace:”，后跟{@link util.format()}格式化消息和堆栈跟踪到代码中的当前位置
             */
            trace(message?: any, ...optionalParams: any[]): void;
            /**
             * The {@link console.warn()} function is an alias for {@link console.error()}.
             * 打印信息前有黄色的感叹号
             */
            warn(message?: any, ...optionalParams: any[]): void;

            // --- Inspector mode only ---
            /**
             * This method does not display anything unless used in the inspector.
             *  Starts a JavaScript CPU profile with an optional label.
             * 此方法不显示任何内容，除非在检查器中使用。
             * 使用可选标签启动JavaScript CPU配置文件
             */
            profile(label?: string): void;
            /**
             * This method does not display anything unless used in the inspector.
             *  Stops the current JavaScript CPU profiling session if one has been started and prints the report to the Profiles panel of the inspector.
             * 停止当前JavaScript CPU分析会话（如果已经启动），并将报告打印到检查器的Profiles面板。
             */
            profileEnd(label?: string): void;
            /**
             * This method does not display anything unless used in the inspector.
             *  Adds an event with the label `label` to the Timeline panel of the inspector.
             * 此方法不显示任何内容，除非在检查器中使用。
             * 将标签为“label”的事件添加到检查器的“时间轴”面板中。
             */
            timeStamp(label?: string): void;
        }

        var console: Console;

        namespace NodeJS {
            interface ConsoleConstructorOptions {
                stdout: WritableStream;
                stderr?: WritableStream;
                ignoreErrors?: boolean;
                colorMode?: boolean | 'auto';
                inspectOptions?: InspectOptions;
            }

            interface ConsoleConstructor {
                prototype: Console;
                new(stdout: WritableStream, stderr?: WritableStream, ignoreErrors?: boolean): Console;
                new(options: ConsoleConstructorOptions): Console;
            }

            interface Global {
                console: typeof console;
            }
        }
    }

    export = console;
}
```

## 参考资料

- [console.spec.whatwg.org](https://console.spec.whatwg.org/)
- [MDN API Console](https://developer.mozilla.org/en-US/docs/Web/API/Console)
