title: 关于代码审查的几点建议
description:
category: CodeReview
tag: CodeReview
-------------------------

Code Review即代码审查是软件开发中常用的手段，它和QA测试相比，更容易发现架构以及时序相关等较难发现的问题，还可以帮助团队成员统一编程风格，提高编程技能等。代码审查被公认为是一个提高代码质量的有效手段。目前很多开发团队虽然进行了代码审查，但是他们可能没有有效、合理的进行代码审查，以致没有很好达到代码审查的目的。近日，BIDS 贸易科技有限公司的CTO Jim Bird 总结了关于代码审查的一些建议。现对这些建议进行了一个全面的梳理，具体内容如下：

####1、代码审查不要太正式

目前，有很多研究表明正式代码的评审会议会延误开发进度和增加开发成本。尽管可能只需要几周的时间进行代码评审，但是只有4%的缺陷是在会议期间发现的，其余所有的权限是靠代码审查者自己发现和处理的。只有采用简短、轻量的代码审查才是有效的发现问题在代码检查,这样的代码审查更适合迭代、增量开发，为开发者提供更快的反馈。

####2、代码审查人员要尽可能少

并不是代码审查人员越多就能发现越多Bug，只有合理数量的审查人员才能够更加有效的地审查代码。研究表明，平均来说，一个代码审查人员能够发现Bug的一半, 第二审稿人会发现剩余新问题的一半。多个人同2个人发现问题的数量没有太大差异，故两个人进行代码审查是比较合适的。另外，还由于社会惰性的存在，更多代码审查人员意味着多人在寻找同样的问题，使得审查人员积极性、主动性不高，更加不利于代码审查工作的有效进行。

####3、需要有经验的开发者进行代码审查

研究充分表明，代码审查的有效性依赖于审查人的技能和对问题领域以及代码的熟悉程度。如果让新加入团队的成员进行代码审查的话，并不利于他们的成长，且对于代码审查来说也是一种非常糟糕的方式。只有擅长阅读代码、程序调试、非常熟悉语言、框架、对应的问题的人才最适合代码审查，才能够高效发现问题、提供更多有价值的反馈。新的、没有经验的开发者只适合检查代码的变化和使用静态分析工具并和另一位评论人员共同代码审查。

####4、实质重于方式

完全按照编码规格标准进行的代码审查是一个浪费开发人员宝贵时间的方式。代码审查的实质是确认代码能够正确的运行，发现安全漏洞、功能错误、代码错误、设计失误、安全验证和防范、恶意代码等。而不是单单按照编码规范完全保证代码格式一致，而丢失了代码审查的实质。

####5、合理安排Bug 和可维护性问题代码的审查时间分配

发现代码中的Bug是很难的，在别人的代码找到的Bug更难。研究表明，代码审查人员找到Bug和可维护性、可读性问题的比例是25:75，故消耗在了代码可读性、可维护性等问题上和Bug上的代码审查时间应该合理分配。

####6、尽量使用静态代码分析工具以提高审查效率

工欲善其事，必先利其器。静态代码分析工具可以帮助程序开发人员自动执行静态代码分析，快速定位代码隐藏错误和缺陷；帮助代码设计人员更专注于分析和解决代码设计缺陷；显著减少在代码逐行检查上花费的时间，提高了软件可靠性并节省软件开发和测试成本。

####7、二八定律处理高风险代码

审查所有的代码并没有太大的意义，应该把审查的重点放在高风险的代码和容易引起高风险的修改或者重构的代码上。旧而复杂、处理敏感数据、处理重要业务逻辑和流程、大规模重构以及刚加入团队的开发者实现的代码都是审查的重点。

####8、从代码审查中尽量获得最大的收益

虽然代码审查是发现Bug、提高开发人员代码编写质量的重要方式，但是它也增加了代码开发成本。如果没有合理、有效的进行代码审查，将有可能影响项目进度和破坏团队文化。故我们要紧抓代码审查的实质性问题，尽早和经常性的进行非正式的代码审查；选择精而少的人员并运用二八定律审查高风险的代码，同时，还需要合理分配Bug以及可维护性问题的代码审查时间，才可以从代码审查中获得最大的收益。
