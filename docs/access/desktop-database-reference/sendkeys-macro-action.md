---
title: Ação da macro EnviarSequênciaDeCaracteres
TOCTitle: SendKeys macro action
ms:assetid: 3b06fcfc-ea64-c780-b5fc-6fc72853f524
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192656(v=office.15)
ms:contentKeyID: 48544275
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm183441
f1_categories:
- Office.Version=v15
ms.openlocfilehash: aa029e3a81670746cdc467ddf7578c5900b58b29
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929031"
---
# <a name="sendkeys-macro-action"></a><span data-ttu-id="d9463-102">Ação da macro EnviarSequênciaDeCaracteres</span><span class="sxs-lookup"><span data-stu-id="d9463-102">SendKeys macro action</span></span>


<span data-ttu-id="d9463-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="d9463-103">**Applies to**: Access 2013, Office 2013</span></span>

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="Observação sobre segurança" alt="Security note" /><span data-ttu-id="d9463-105"><strong>Observação de segurança</strong></span><span class="sxs-lookup"><span data-stu-id="d9463-105"><strong>Security Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d9463-p101">
      Avoid using the <strong>SendKeys</strong> statement or an AutoKeys macro with sensitive or confidential information. A malicious user could intercept the keystrokes and compromise the security of your computer and data.
</span><span class="sxs-lookup"><span data-stu-id="d9463-p101">Avoid using the <strong>SendKeys</strong> statement or an AutoKeys macro with sensitive or confidential information. A malicious user could intercept the keystrokes and compromise the security of your computer and data.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d9463-108">Use a ação **EnviarSequênciadeCaracteres** para enviar pressionamentos de teclas para o Microsoft Access ou para um aplicativos ativo baseado no Windows.</span><span class="sxs-lookup"><span data-stu-id="d9463-108">You can use the **SendKeys** action to send keystrokes directly to Microsoft Access or to an active Windows-based application.</span></span>


> [!NOTE]
> <P><span data-ttu-id="d9463-p102">[!OBSERVAçãO] This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span><span class="sxs-lookup"><span data-stu-id="d9463-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="d9463-111">Configuração</span><span class="sxs-lookup"><span data-stu-id="d9463-111">Setting</span></span>

<span data-ttu-id="d9463-112">A ação **EnviarSequênciaDeCaracteres** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="d9463-112">The **SendKeys** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d9463-113">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="d9463-113">Action argument</span></span></p></th>
<th><p><span data-ttu-id="d9463-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="d9463-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d9463-115"><strong>Pressionamentos de teclas</strong></span><span class="sxs-lookup"><span data-stu-id="d9463-115"><strong>Keystrokes</strong></span></span></p></td>
<td><p><span data-ttu-id="d9463-p103">Os pressionamentos de teclas a serem processados pelo Access ou pelo aplicativo. Insira-os na caixa <strong>Pressionamentos de Teclas</strong> na seção <strong> Argumentos da Ação</strong> do painel Construtor de Macros. Você pode digitar até 255 caracteres. Este é um argumento obrigatório.</span><span class="sxs-lookup"><span data-stu-id="d9463-p103">The keystrokes you want Access or the application to process. Enter the keystrokes in the <strong>Keystrokes</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. You can type up to 255 characters. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9463-120"><strong>Wait</strong></span><span class="sxs-lookup"><span data-stu-id="d9463-120"><strong>Wait</strong></span></span></p></td>
<td><p><span data-ttu-id="d9463-p104">Especifica se a macro deve ser pausada enquanto os pressionamentos de teclas são processados. Clique em <strong>Sim</strong> (para pausar) ou em <strong>Não</strong> (para não pausar). O padrão é <strong>Não</strong>.</span><span class="sxs-lookup"><span data-stu-id="d9463-p104">Specifies whether the macro should pause until the keystrokes have been processed. Click <strong>Yes</strong> (to pause) or <strong>No</strong> (to not pause). The default is <strong>No</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d9463-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="d9463-124">Remarks</span></span>

<span data-ttu-id="d9463-125">O Access processa os pressionamentos de teclas recebidos por meio da ação **EnviarSequênciadeCaracteres** exatamente como se você os tivesse digitado diretamente em uma janela do Access.</span><span class="sxs-lookup"><span data-stu-id="d9463-125">Access processes the keystrokes it receives through the **SendKeys** action exactly as if you had typed them directly in an Access window.</span></span>

<span data-ttu-id="d9463-126">Para especificar os pressionamentos de teclas, use a mesma sintaxe que usaria para a instrução **EnviarSequênciadeCaracteres**.</span><span class="sxs-lookup"><span data-stu-id="d9463-126">To specify the keystrokes, use the same syntax as you would for the **SendKeys** statement.</span></span>


> [!NOTE]
> <P><span data-ttu-id="d9463-127">[!OBSERVAçãO] É possível a ocorrência de erro quando o argumento <STRONG>Pressionamentos de teclas</STRONG> contém sintaxe incorreta, erros ortográficos ou outros valores inadequados para a janela da qual os pressionamentos de teclas são enviados.</span><span class="sxs-lookup"><span data-stu-id="d9463-127">An error can occur if the <STRONG>Keystrokes</STRONG> argument contains incorrect syntax, misspelled text, or other values that aren't appropriate for the window the keystrokes are sent to.</span></span></P>



<span data-ttu-id="d9463-p105">Você pode usar esta ação para inserir informações em uma caixa de diálogo, principalmente se não quiser interromper a macro para responder manualmente à caixa de diálogo. Algumas ações do Access, como **ArquivoComCópia** e **EncontrarRegistro**, selecionam automaticamente as opções de algumas caixas de diálogo de uso frequente. Use a ação **EnviarSequênciaDeCaracteres** para selecionar opções em caixas de diálogo de uso menos frequente.</span><span class="sxs-lookup"><span data-stu-id="d9463-p105">You can use this action to enter information in a dialog box, particularly if you don't want to interrupt the macro to respond manually to the dialog box. Some Access actions, such as **PrintOut** and **FindRecord**, automatically select the options in certain frequently used dialog boxes. You can use the **SendKeys** action to select the options in less commonly used dialog boxes.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="d9463-131">Como a caixa de diálogo suspende a macro, coloque a ação <STRONG>EnviarSequênciaDeCaracteres</STRONG> antes da ação que abre a caixa de diálogo e defina o argumento <STRONG>Aguardar</STRONG> como <STRONG>Não</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="d9463-131">Because the dialog box suspends the macro, you must put the <STRONG>SendKeys</STRONG> action before the action that causes the dialog box to open and set the <STRONG>Wait</STRONG> argument to <STRONG>No</STRONG>.</span></span></P>
> <LI>
> <P><span data-ttu-id="d9463-p106">O intervalo dos pressionamentos de teclas para alcançar o Access ou outro aplicativo pode ser complicado. Por isso, se houver outros métodos (como a ação <STRONG>EncontrarRegistro</STRONG> ) que você possa usar para obter a tarefa desejada, é recomendável usá-lo no lugar da ação <STRONG>EnviarSequênciadeCaracteres</STRONG> para preencher as opções de uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d9463-p106">The timing of the keystrokes reaching Access or another application can be tricky. As a result, it's recommended that if there's some other method (such as the <STRONG>FindRecord</STRONG> action) you can use to achieve a desired task, use that method rather than using the <STRONG>SendKeys</STRONG> action to fill in the options in a dialog box.</span></span></P></LI></UL>



<span data-ttu-id="d9463-134">Se quiser enviar mais de 255 caracteres para o Access ou outro aplicativo baseado no Windows, use várias ações **EnviarSequênciaDeCaracteres** em sucessão, em uma macro.</span><span class="sxs-lookup"><span data-stu-id="d9463-134">If you want to send more than 255 characters to Access or another Windows-based application, you can use several **SendKeys** actions in succession in a macro.</span></span>

<span data-ttu-id="d9463-p107">Se usar a **EnviarSequênciadeCaracteres** para enviar pressionamentos de teclas, isso disparará os eventos **ApertarTecla**, **LiberarTecla** e **PressionarTecla**. O envio de pressionamentos de teclas não ANSI (por exemplo, uma tecla de função) não dispara o evento **PressionarTecla**.</span><span class="sxs-lookup"><span data-stu-id="d9463-p107">Using the **SendKeys** action to send keystrokes triggers the appropriate **KeyDown**, **KeyUp**, and **KeyPress** events. Sending non-ANSI keystrokes (such as a function key) doesn't trigger the **KeyPress** event.</span></span>

<span data-ttu-id="d9463-p108">Esta ação não está disponível em um módulo do VBA (Visual Basic for Applications). Em vez disso, use a instrução **SendKeys**.</span><span class="sxs-lookup"><span data-stu-id="d9463-p108">This action isn't available from a Visual Basic for Applications (VBA) module. Use the **SendKeys** statement instead.</span></span>

