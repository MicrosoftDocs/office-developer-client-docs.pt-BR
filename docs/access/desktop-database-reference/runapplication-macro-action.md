---
title: Ação da macro ExecutarAplicativo
TOCTitle: RunApplication macro action
ms:assetid: 29967e6e-c441-b115-3ee6-2299b8a3bc25
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192038(v=office.15)
ms:contentKeyID: 48543885
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm93359
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: e7bf54934c6be215b2be5f32160d74fc2b4ab346
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721784"
---
# <a name="runapplication-macro-action"></a><span data-ttu-id="5f193-102">Ação da macro ExecutarAplicativo</span><span class="sxs-lookup"><span data-stu-id="5f193-102">RunApplication macro action</span></span>

<span data-ttu-id="5f193-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="5f193-103">**Applies to**: Access 2013, Office 2013</span></span>

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="Observação sobre segurança" alt="Security note" /><span data-ttu-id="5f193-105"><strong>Observação de segurança</strong></span><span class="sxs-lookup"><span data-stu-id="5f193-105"><strong>Security Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5f193-p101">Use caution when running executable files or code in macros or applications. Executable files or code can be used to carry out actions that might compromise the security of your computer and data.</span><span class="sxs-lookup"><span data-stu-id="5f193-p101">Use caution when running executable files or code in macros or applications. Executable files or code can be used to carry out actions that might compromise the security of your computer and data.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5f193-p102">Você pode usar a ação **ExecutarAplicativo** para executar, no Microsoft Access, um aplicativo baseado no Microsoft Windows ou no MS-DOS, como Microsoft Excel, Microsoft Word ou Microsoft PowerPoint. Por exemplo, é possível colar os dados de uma planilha do Excel no banco de dados do Access.</span><span class="sxs-lookup"><span data-stu-id="5f193-p102">You can use the **RunApplication** action to run a Microsoft Windows-based or MS-DOS-based application, such as Microsoft Excel, Microsoft Word, or Microsoft PowerPoint, from within Microsoft Access. For example, you may want to paste Excel spreadsheet data into your Access database.</span></span>

> [!NOTE]
> <span data-ttu-id="5f193-110">[!OBSERVAçãO] This action will not be allowed if the database is not trusted.</span><span class="sxs-lookup"><span data-stu-id="5f193-110">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="5f193-111">Configuração</span><span class="sxs-lookup"><span data-stu-id="5f193-111">Setting</span></span>

<span data-ttu-id="5f193-112">A ação **ExecutarAplicativo** tem o seguinte argumento.</span><span class="sxs-lookup"><span data-stu-id="5f193-112">The **RunApplication** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5f193-113">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="5f193-113">Action argument</span></span></p></th>
<th><p><span data-ttu-id="5f193-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="5f193-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f193-115"><strong>Linha de comando</strong></span><span class="sxs-lookup"><span data-stu-id="5f193-115"><strong>Command Line</strong></span></span></p></td>
<td><p><span data-ttu-id="5f193-p103">A linha de comando é usada para iniciar o aplicativo (incluindo o caminho e todos os demais parâmetros necessários, como as opções que permitem executar o aplicativo em um determinado modo). Digite a linha de comando na caixa <strong>Linha de Comando</strong>, na seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. Este é um argumento obrigatório.</span><span class="sxs-lookup"><span data-stu-id="5f193-p103">The command line used to start the application (including the path and any other necessary parameters, such as switches that run the application in a particular mode). Enter the command line in the <strong>Command Line</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. This is a required argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="5f193-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f193-119">Remarks</span></span>

<span data-ttu-id="5f193-p104">O aplicativo selecionado com essa ação é carregado e executado em primeiro plano. A macro que contém essa ação continuará a ser executada depois de iniciado o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5f193-p104">The application selected with this action loads and runs in the foreground. The macro containing this action continues to run after starting the application.</span></span>

<span data-ttu-id="5f193-p105">Você pode transferir dados entre o outro aplicativo e o Access usando o recurso DDE (troca dinâmica de dados) do Microsoft Windows ou a área de transferência. A ação **EnviarSequênciadeCaracteres** pode ser utilizada para enviar pressionamentos de teclas ao outro aplicativo (embora o DDE seja um método mais eficiente de transferência de dados). Também é possível compartilhar dados entre vários aplicativos usando a automação.</span><span class="sxs-lookup"><span data-stu-id="5f193-p105">You can transfer data between the other application and Access by using the Microsoft Windows dynamic data exchange (DDE) facility or the Clipboard. You can use the **SendKeys** action to send keystrokes to the other application (although DDE is a more efficient method for transferring data). You can also share data among applications by using automation.</span></span>

<span data-ttu-id="5f193-125">Os aplicativos baseados no MS-DOS são executados em uma janela do MS-DOS no ambiente Windows.</span><span class="sxs-lookup"><span data-stu-id="5f193-125">MS-DOS-based applications run in an MS-DOS window within the Windows environment.</span></span>

<span data-ttu-id="5f193-126">Nos sistemas operacionais Windows, há muitas maneiras de executar um aplicativo, incluindo a inicialização do programa no Windows Explorer, usando o comando **Executar** no menu **Iniciar** ou clicando duas vezes em um ícone de programa na Área de Trabalho do Windows.</span><span class="sxs-lookup"><span data-stu-id="5f193-126">In Windows operating systems, there are a number of ways to run an application, including starting the program from the Windows Explorer, using the **Run** command on the **Start** menu, and double-clicking a program icon on the Windows Desktop.</span></span>

<span data-ttu-id="5f193-p106">Não é possível executar a ação **ExecutarAplicativo** em módulos do VBA (Visual Basic for Applications). Em vez disso, use a função **Shell** do VBA.</span><span class="sxs-lookup"><span data-stu-id="5f193-p106">You can't run the **RunApplication** action in a Visual Basic for Applications (VBA) module. Use the VBA **Shell** function instead.</span></span>

