---
title: Ação da macro EnviarEmail
TOCTitle: SendEmail macro action
ms:assetid: 84ff6b46-d239-4716-9964-5b909656d347
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196780(v=office.15)
ms:contentKeyID: 48546046
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: aa783dcc7ad02cc36b14ef9ef97436cb1ad88e4a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924684"
---
# <a name="sendemail-macro-action"></a><span data-ttu-id="8f51b-102">Ação da macro EnviarEmail</span><span class="sxs-lookup"><span data-stu-id="8f51b-102">SendEmail macro action</span></span>


<span data-ttu-id="8f51b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="8f51b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8f51b-104">A ação **EnviarEmail** envia uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="8f51b-104">The **SendEmail** action sends an e-mail message.</span></span>


> [!NOTE]
> <P><span data-ttu-id="8f51b-105">[!OBSERVAçãO] A ação <STRONG>EnviarEmail</STRONG> está disponível somente em Macros de Dados.</span><span class="sxs-lookup"><span data-stu-id="8f51b-105">The <STRONG>SendEmail</STRONG> action is available only in Data Macros.</span></span></P>



## <a name="setting"></a><span data-ttu-id="8f51b-106">Configuração</span><span class="sxs-lookup"><span data-stu-id="8f51b-106">Setting</span></span>

<span data-ttu-id="8f51b-107">A ação **EnviarEmail** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="8f51b-107">The **SendEmail** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8f51b-108">Argumento</span><span class="sxs-lookup"><span data-stu-id="8f51b-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="8f51b-109">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="8f51b-109">Required</span></span></p></th>
<th><p><span data-ttu-id="8f51b-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="8f51b-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8f51b-111"><strong>To</strong></span><span class="sxs-lookup"><span data-stu-id="8f51b-111"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="8f51b-112">Sim</span><span class="sxs-lookup"><span data-stu-id="8f51b-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="8f51b-113">Os destinatários da mensagem cujos nomes você deseja colocar na linha <strong>para</strong> da mensagem. Separe os nomes dos destinatários especificados neste argumento (e nos argumentos <em>Cc</em> e <em>Cco</em> ) com um ponto e vírgula (;).</span><span class="sxs-lookup"><span data-stu-id="8f51b-113">The recipients of the message whose names you want to put on the <strong>To</strong> line in the message.Separate the recipient names that you specify in this argument (and in the <em>Cc</em> and <em>Bcc</em> arguments) with a semicolon (;).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f51b-114"><strong>Cc</strong></span><span class="sxs-lookup"><span data-stu-id="8f51b-114"><strong>Cc</strong></span></span></p></td>
<td><p><span data-ttu-id="8f51b-115">Não</span><span class="sxs-lookup"><span data-stu-id="8f51b-115">No</span></span></p></td>
<td><p><span data-ttu-id="8f51b-116">Os destinatários da mensagem cujos nomes você deseja colocar na Cc (&quot;cópia carbono&quot;) linha da mensagem.</span><span class="sxs-lookup"><span data-stu-id="8f51b-116">The message recipients whose names you want to put on the Cc (&quot;carbon copy&quot;) line in the message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f51b-117"><strong>Cco</strong></span><span class="sxs-lookup"><span data-stu-id="8f51b-117"><strong>Bcc</strong></span></span></p></td>
<td><p><span data-ttu-id="8f51b-118">Não</span><span class="sxs-lookup"><span data-stu-id="8f51b-118">No</span></span></p></td>
<td><p><span data-ttu-id="8f51b-119">Os destinatários da mensagem cujos nomes você deseja colocar na Cco (&quot;cópia oculta&quot;) linha da mensagem.</span><span class="sxs-lookup"><span data-stu-id="8f51b-119">The message recipients whose names you want to put on the Bcc (&quot;blind carbon copy&quot;) line in the message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f51b-120"><strong>Subject</strong></span><span class="sxs-lookup"><span data-stu-id="8f51b-120"><strong>Subject</strong></span></span></p></td>
<td><p><span data-ttu-id="8f51b-121">Não</span><span class="sxs-lookup"><span data-stu-id="8f51b-121">No</span></span></p></td>
<td><p><span data-ttu-id="8f51b-p101">O assunto da mensagem. Esse texto aparece na linha <strong>Assunto</strong> da mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="8f51b-p101">The subject of the message. This text appears on the <strong>Subject</strong> line in the message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f51b-124"><strong>Body</strong></span><span class="sxs-lookup"><span data-stu-id="8f51b-124"><strong>Body</strong></span></span></p></td>
<td><p><span data-ttu-id="8f51b-125">Não</span><span class="sxs-lookup"><span data-stu-id="8f51b-125">No</span></span></p></td>
<td><p><span data-ttu-id="8f51b-p102">O texto que você deseja incluir no corpo principal da mensagem de email. Se você deixar esse argumento em branco, nenhum texto adicional será incluído na mensagem.</span><span class="sxs-lookup"><span data-stu-id="8f51b-p102">The text that you want to include in the main body of the mail message. If you leave this argument blank, no additional text is included in the message.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="8f51b-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="8f51b-128">Remarks</span></span>

<span data-ttu-id="8f51b-129">A ação **EnviarEmail** está disponível somente nos eventos de macro **[Após Exclusão](after-delete-macro-event.md)**, **[Após Inserir](after-insert-macro-event.md)** e **[Após Atualizar](after-update-macro-event.md)**.</span><span class="sxs-lookup"><span data-stu-id="8f51b-129">The **SendEmail** action is available only in the **[After Delete](after-delete-macro-event.md)**, **[After Insert](after-insert-macro-event.md)**, and **[After Update](after-update-macro-event.md)** macro events.</span></span>

<span data-ttu-id="8f51b-130">A ação **EnviarEmail** não exibe a mensagem para edição.</span><span class="sxs-lookup"><span data-stu-id="8f51b-130">The **SendEmail** action does not display the message for editing.</span></span>

