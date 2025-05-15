

**引言**

WebDAV（Web分布式创作与版本控制）是HTTP协议的扩展，它允许用户像管理本地文件一样在远程服务器上管理文件，极大地便利了文件同步和与各种应用程序的集成 1。随着用户对云存储解决方案需求的日益增长，对支持WebDAV的云存储服务的需求也随之增加，这为用户提供了更强的灵活性和对其数据的控制 2。本报告旨在识别和比较当前可用的支持WebDAV协议的免费云存储服务，全面分析其功能、限制以及对不同用户需求的适用性。

**主要的免费网盘服务**

根据研究资料，以下是一些提供免费计划的主要网盘服务：

- MEGA 3：提供慷慨的初始免费存储空间。
- Google Drive 3：广泛使用，并与Google生态系统集成。
- pCloud 3：以安全性和媒体功能而闻名。
- OneDrive 3：与Microsoft服务集成。
- Box 4：在商业领域广受欢迎。
- Yandex Disk 2：在俄语地区较为流行。
- MyDrive 2：一个开源选项。
- Sync.com 4：专注于安全和隐私。
- Icedrive 4：以速度和界面著称。
- TeraBox 4：提供非常大的免费存储空间。
- Filen 4：强调安全性。
- Koofr 4：集成多个云存储账户。
- MediaFire 5：适合分享大型文件。
- Internxt 4：注重隐私，提供终身套餐。
- Hivenet 3：专注于分布式存储和可持续性。
- Rakuten Drive 5：提供文件共享权限。
- Degoo 4：提供慷慨的存储空间，但带有广告。
- Blomp 10：提供免费无限视频存储。
- Jottacloud 5：付费计划提供无限存储。
- Proton Drive 5：专注于隐私和安全性。
- iDriveSync 2：在Zotero文档中提到。
- CloudMe 2：支持WebDAV。
- DriveOnWeb 2：文档为德语。
- HiDrive 2：提供免费存储和WebDAV。
- Storegate 2：提供WebDAV支持。
- Cloudsafe 40：过去曾提供免费WebDAV。
- Swissdisk 2：提供免费存储和WebDAV。

如此众多的免费网盘服务反映了市场竞争的激烈程度，但关键在于根据WebDAV支持进行筛选，这将大大缩小可行的选择范围。既有成熟的服务提供商，也有较小的专业服务，这表明了在免费存储和功能方面存在不同的策略。

**验证免费计划的WebDAV支持**

接下来，我们将分析每个已识别的服务提供商，以确定其免费计划是否支持WebDAV。

- **pCloud：** 研究资料 35、95、96、97、95 和 35 确认，**自2022年2月11日起，免费pCloud账户不再支持WebDAV。** 希望使用WebDAV的用户需要升级到高级计划。资料 98 表明 DAVx⁵ 已成功通过 pCloud WebDAV 测试，但这可能指的是付费账户。资料 99 提到 WebDAV 是 pCloud 的一部分，但未具体说明计划类型。资料 100 提到在不购买任何东西的情况下使用 pCloud 进行同步，这可能表明对于免费用户的 WebDAV 存在混淆或过时的信息。
    - **分析：** pCloud免费计划取消WebDAV支持是一个重要的变化，许多较旧的资源可能仍然将pCloud列为免费的WebDAV选项，因此报告需要强调这一最近的变更。这可能会导致用户错误地假设存在免费的WebDAV支持。资料 98 中提到 DAVx⁵ 测试，这表明底层的 WebDAV 功能可能仍然存在，但现在需要付费才能使用。用户的查询明确要求 _当前_ 可用的选项，这使得这一历史变更成为关键信息。
- **Box：** 资料 36、40、101、102、103、104、105、106、107 和 37 表明 Box 和 WebDAV 的情况复杂且不断变化。资料 40 指出 WebDAV 适用于付费客户。资料 103 和 104 确认 **Box 已于2023年4月28日终止对 WebDAV 的支持。** 虽然一些用户可能继续使用它，但它已不再受官方支持，尤其是对于免费账户（105、106）。资料 36 建议使用 MultCloud 作为一种变通方法。
    - **分析：** 与 pCloud 类似，Box 对免费用户的 WebDAV 支持不可靠或不存在。报告应明确说明官方支持的终止。资料 36 中提到通过 MultCloud 的变通方法，这表明即使在服务提供商正式停止支持后，用户对 WebDAV 访问的需求仍然存在。这也引入了使用第三方工具来弥合差距的概念，这可能对某些用户来说是一种有价值的替代方案。
- **MEGA：** 资料 12 和 12 明确指出 **MEGA 通过其命令行工具 MEGA CMD 支持 WebDAV。** 资料 13 证实了这一点。然而，资料 15 指出由于客户端加密，MEGA 不直接支持 WebDAV，并建议使用其同步客户端。资料 108 提到在 Linux 上使用 mega-cmd-server 设置 WebDAV。资料 14 提供了即使对于免费账户，也可以使用 MEGAcmd 和 WebDAV 流式传输整个 MEGA 云驱动器的说明。
    - **分析：** MEGA 对 WebDAV（12、12、13、108、14）的处理方式是独特的。虽然他们的主要重点是通过端到端加密来保证安全性，但他们通过一个单独的命令行工具提供 WebDAV 访问。这暗示了用户友好性和功能性之间的权衡。即使对于免费账户也可用这一事实使 MEGA 成为那些熟悉命令行界面或需要其特定功能的用户的一个强有力的竞争者。与资料 15 的冲突可能表明他们的标准应用程序中缺少直接的 WebDAV 集成。
- **Yandex Disk：** 资料 2 和 2 将 Yandex Disk 列为支持 WebDAV 的服务。资料 16、17、19、109、20、22、110 和 18 进一步证实了这一点，一些资料中提供了 WebDAV URL（例如，2）。资料 16 提到 WebDAV 支持。然而，资料 19 和 20 指出，虽然支持 WebDAV，但它可能受到限制或被认为是非官方功能，可能导致速度缓慢和不稳定。资料 23 报告了2023年 Yandex Disk WebDAV 的“402 - 需要付款”错误，这表明可能存在更改或区域限制。
    - **分析：** Yandex Disk 的 WebDAV 支持（2、2、16、17、19、109、20、22、110、18、16）呈现出复杂的情况。虽然官方列为受支持，但关于限制（19、20）、潜在不可靠（22）甚至付款要求（23）的众多报告表明，其免费 WebDAV 访问可能不是一种始终积极的体验。提到它是“非官方的”（19、20）进一步表明用户应谨慎行事，并为潜在问题做好准备。
- **MyDrive (Softronics.ch)：** 资料 26、24、27、25、2、60 和 28 表明 **MyDrive (来自 Softronics.ch) 在其2GB免费计划中支持 WebDAV。** 资料 26 中提到了 WebDAV URL。资料 62 也将 MyDrive 列为支持 WebDAV 的服务。
    - **分析：** 根据资料（26、24、27、25、2、60、28、62），MyDrive 似乎是一个更可靠的免费 WebDAV 选项。提供 WebDAV URL 甚至故障排除步骤（26）表明了一种更直接和受支持的方法。然而，2GB 的免费存储限制可能对许多用户来说是一个制约因素。关于它与 OmniFocus 的积极使用反馈（25）表明了它可能适用于特定的应用程序集成。
- **Sync.com：** 资料 4 未明确提及 Sync.com 免费计划的 WebDAV。资料 5 将 Sync.com 列为“最佳安全性”，但未提及 WebDAV。资料 81 详细介绍了免费计划的功能，但未列出 WebDAV。
    - **分析：** 在 Sync.com 免费计划（4、5、81）的上下文中，没有任何提及 WebDAV 支持的信息，这强烈表明它要么未提供，要么不是一个突出的功能。考虑到他们对安全性的关注，他们可能会优先考虑他们自己的加密协议，而不是像 WebDAV 这样的标准协议，用于免费用户。
- **Icedrive：** 资料 4 列出了 Icedrive，但未指定免费计划的 WebDAV。资料 5 未提及 WebDAV。资料 8 指出 Icedrive 在操作系统集成方面是最好的，但没有提及免费的 WebDAV。资料 15 提到 Icedrive 从2021年1月1日起逐步淘汰 WebDAV 支持，但后来的编辑说他们将保留它。
    - **分析：** 关于 Icedrive 免费 WebDAV 支持的信息是矛盾且不明确的（4、5、8、15）。最初关于逐步淘汰支持的迹象引起了人们对其作为长期免费选项的可靠性的担忧。缺乏对免费层的明确确认表明最好考虑其他更明确支持的服务。
- **TeraBox：** 资料 86 和 88 表明 TeraBox 可能不提供直接的 WebDAV 支持，访问主要通过他们自己的客户端。
    - **分析：** 尽管 TeraBox 提供了异常大的免费存储空间（4、30、9、45、10、11、84、85、86、87、47、88、89、90、91），但缺乏对 WebDAV 支持的提及（86、88）表明它可能不符合用户对 WebDAV 访问的特定要求。
- **Filen：** 资料 6 提到 Filen 是免费存储的推荐选项，但未提及 WebDAV。资料 111 明确指出 Filen 不支持 WebDAV。
    - **分析：** Filen 虽然专注于安全性（4、6、92、111），但不支持 WebDAV，因此不适合用户的查询。
- **Koofr：** 资料 93 提到 Koofr + WebDAV 效果很好，资料 2 将 Koofr 列为免费的 WebDAV 服务。
    - **分析：** Koofr 似乎是一个很有希望的选项（4、5、30、6、45、93、11、2），用户报告其 WebDAV 功能具有积极的使用体验（93）。与其他云账户的集成（30）也可能对某些用户来说是一个有价值的功能。
- **MediaFire：** 资料 38 明确指出 **MediaFire 不直接支持 WebDAV。** 它建议使用 MultCloud 作为中介。
    - **分析：** MediaFire 虽然擅长分享大型文件（5、6、38、45、10、11、38），但未提供直接的 WebDAV 支持（38），需要借助第三方工具。
- **Internxt、Hivenet、Rakuten Drive、Degoo、Blomp、Jottacloud、Proton Drive：** 根据提供的资料，这些服务的免费计划中没有明确提及 WebDAV 支持。
- **iDriveSync、CloudMe、DriveOnWeb、HiDrive、Storegate、Cloudsafe、Swissdisk：** 这些服务在初步筛选中被认为可能提供免费的 WebDAV，将在比较分析部分进行分析。

**免费WebDAV网盘服务比较分析**

下表总结了已识别的免费WebDAV支持服务提供商的信息：

|   |   |   |   |
|---|---|---|---|
|**名称**|**免费存储限制**|**WebDAV URL (如果可用)**|**主要限制/注意事项**|
|MEGA|20 GB|通过 MEGA CMD 提供|需要使用命令行工具；免费账户有带宽限制|
|Yandex Disk|高达 20 GB|例如：[https://webdav.yandex.ru/zotero](https://webdav.yandex.ru/zotero)|可能存在限速和不稳定性；可能是非官方功能；可能存在区域限制或账户验证要求|
|MyDrive|2 GB|瑞士：[https://mydrive.ch/webdav.php](https://mydrive.ch/webdav.php)；欧盟：[https://eu.mydrive.ch/webdav.php](https://eu.mydrive.ch/webdav.php)|存储空间较小；某些用户报告初始设置或特定应用程序存在问题|
|Koofr|10 GB (Zotero wiki 提到 2 GB)|[https://app.koofr.net/dav/Koofr/zotero](https://app.koofr.net/dav/Koofr/zotero)|报告的免费存储空间量可能不一致|
|HiDrive|5 GB (可通过推荐增加到 10 GB)|[https://webdav.hidrive.strato.com/users/](https://webdav.hidrive.strato.com/users/){用户名}/zotero|对于某些用户来说，免费存储空间可能较低|
|Swissdisk|50 MB|[www.swissdisk.com](https://www.swissdisk.com/)|免费存储空间非常有限，不适合一般文件存储|
|iDriveSync|10 GB|[https://dav.idrivesync.com/zotero](https://dav.idrivesync.com/zotero)|用户报告存在问题；文档建议不要广泛使用|
|CloudMe|3 GB (可通过推荐增加)|[https://webdav.cloudme.com/](https://webdav.cloudme.com/){用户名}/xios/zotero|用户报告同步错误；可能已停止服务|
|DriveOnWeb|3 GB|[https://storage.driveonweb.de/probdav/zotero](https://storage.driveonweb.de/probdav/zotero)|文档为德语|
|Storegate|2 GB|[https://webdav1.storegate.com/](https://webdav1.storegate.com/){用户名}/home/{用户名}/zotero|免费存储空间较小|

**各服务提供商详细讨论**

- **MEGA：** 提供 20 GB 的免费存储空间 3，并且可以通过完成某些任务来扩展 3。免费用户可以通过 MEGA CMD 命令行工具设置 WebDAV 访问 12，该工具需要一定的技术知识。MEGA 通常被认为是可靠的 6，速度也很快 5。虽然标准应用程序不直接支持 WebDAV 15，但 MEGA CMD 提供了所需的功能。免费账户的主要限制是带宽限制 3。对于需要更大存储空间且熟悉命令行的用户来说，MEGA 是一个有吸引力的选择。
- **Yandex Disk：** 提供高达 20 GB 的免费存储空间（注册时 10 GB，加上奖励）2。它列出了支持 WebDAV 2，并提供了 WebDAV URL 2。然而，用户报告存在限速和速度缓慢的问题 18，并且可能不稳定 22。2023年，一些用户报告了“需要付款”的错误 23。虽然官方应用程序运行良好 19，但 WebDAV 的可靠性可能较低。免费 WebDAV 支持可能被视为非官方功能 19，并且可能存在区域限制或账户验证要求 23。尽管提供了不错的免费存储空间和 WebDAV，但 Yandex Disk 的 WebDAV 访问的可靠性和性能似乎令人担忧。用户应注意潜在的速度限制和可能的服务变更。
- **MyDrive：** 提供 2 GB 的免费存储空间 2。它支持 WebDAV，并提供了瑞士和欧盟地区的 WebDAV URL 26。MyDrive 甚至提供了修复 Windows 问题的步骤 26。据报告，MyDrive 在 OmniFocus 同步方面表现良好 25，但一些用户报告了初始速度较慢的问题 25。MyDrive 相对容易使用 28，并支持各种访问方式 26。其主要限制是免费存储空间较小。一些用户报告了初始设置或特定应用程序的问题 25。MyDrive 为那些存储需求较小的用户或需要同步特定应用程序数据的用户提供了一个直接的免费 WebDAV 选项。
- **Koofr：** 提供 10 GB 的免费存储空间 4，尽管 Zotero wiki 提到的是 2 GB 2。Koofr 支持 WebDAV，并提供了 WebDAV URL 2。设置说明也可用 2。它通常被认为是可靠的 29，但最近几周有一些关于问题的报告 23。Koofr 的 WebDAV 安全性实现良好 29，并且可以轻松集成其他云账户 30。用户报告了良好的同步体验 31。需要注意的是，报告的免费存储空间量可能不一致。总体而言，Koofr 似乎是一个可靠的免费 WebDAV 选项，具有不错的存储限制和良好的用户反馈。
- **HiDrive：** 提供 5 GB 的免费存储空间，可以通过推荐增加到 10 GB 2。它支持 WebDAV，并提供了 WebDAV URL 2。研究资料中没有关于其可靠性和性能的具体细节。HiDrive 支持各种访问方式 32。对于某些用户来说，免费存储空间可能较低。HiDrive 提供免费的 WebDAV 支持，存储限制适中，可能适合微软生态系统中的用户。
- **Swissdisk：** 提供 50 MB 的免费存储空间 33。它支持 WebDAV，并提供了 WebDAV URL 33。据报告，Swissdisk 是一项专业且可靠的服务 33，但其非常有限的免费存储空间使其不适合一般文件存储，更适合用于同步 OmniFocus 数据等特定用途。
- **iDriveSync：** 提供 10 GB 的免费存储空间 2，并提供了 WebDAV URL 2。然而，用户报告存在问题 2，其文档建议不要广泛使用 2。基于用户反馈，其用户体验可能存在问题，并且存在可靠性问题。iDriveSync 的免费 WebDAV 支持似乎不可靠，不建议长期使用。
- **CloudMe：** 提供 3 GB 的免费存储空间，可以通过推荐增加 2。它支持 WebDAV，并提供了 WebDAV URL 2。用户报告了 WebDAV 的同步错误 2，并且资料 23 表明 WebDAV 不再起作用。CloudMe 的免费 WebDAV 支持似乎不可靠，并且可能已停止服务。
- **DriveOnWeb：** 提供 3 GB 的免费存储空间 2，并提供了 WebDAV URL 2。研究资料中没有关于其可靠性和性能的具体细节。其文档为德语 2，这对于非德语用户来说可能存在语言障碍。
- **Storegate：** 提供 2 GB 的免费存储空间 2，并提供了 WebDAV URL 2。研究资料中没有关于其可靠性和性能的具体细节。其免费存储空间较小。

**探索替代方案和变通方法**

用户还可以考虑使用第三方多云管理工具，如 MultCloud 6，即使云存储提供商的免费计划不直接支持 WebDAV，也可以通过这些工具访问云存储（例如，MediaFire，可能还有 Google Drive、OneDrive、Box）。MultCloud 充当桥梁，为 MediaFire 等服务启用 WebDAV 访问。然而，使用此类第三方服务也存在潜在的成本和安全问题。用户可能需要为高级功能或更高的使用量付费，并且需要注意授予第三方应用程序对其云存储账户的访问权限所带来的潜在安全风险。

此外，还可以考虑自托管 WebDAV 服务器并将其连接到免费云存储的 API，但这涉及到相当的技术复杂性 23。自托管提供了最大的控制权，但需要大量的技术专业知识进行设置和维护。这种方法可能适合高级用户或那些有特定安全要求的用户。

**结论与建议**

综上所述，目前看来支持WebDAV的免费网盘服务包括：MEGA（通过MEGA CMD）、Yandex Disk、MyDrive、Koofr、HiDrive、Swissdisk、iDriveSync（谨慎使用）、CloudMe（谨慎使用）、DriveOnWeb和Storegate。

根据不同的用户优先级，可以提出以下建议：

- **最大免费存储空间：** MEGA（通过 MEGA CMD）提供最大的免费存储空间和 WebDAV 访问，其次是 Yandex Disk（但可能存在可靠性问题）。
- **易用性：** MyDrive 和 Koofr 似乎提供更直接的 WebDAV 体验。
- **可靠性：** 根据目前的信息，MyDrive 和 Koofr 可能比 Yandex Disk 更可靠。Swissdisk 可靠但存储空间非常有限。
- **特定使用场景：** Swissdisk 适用于存储需求极小的 WebDAV 访问，例如特定应用程序的数据同步；MEGA 适用于熟悉命令行工具且需要更大存储空间的用户。

鉴于免费服务的动态特性，建议用户在选择解决方案之前，直接与服务提供商核实当前的 WebDAV 支持和条款。还建议使用用户的特定客户端应用程序测试 WebDAV 连接。用户还应考虑其安全和隐私需求以及云存储提供商的声誉。