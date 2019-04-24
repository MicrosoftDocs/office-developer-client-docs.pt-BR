---
title: Ação da macro EnviarEmail
TOCTitle: SendEmail macro action
ms:assetid: 84ff6b46-d239-4716-9964-5b909656d347
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196780(v=office.15)
ms:contentKeyID: 48546046
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c0fa220b3088cde46b0e82631c06520afd839c64
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314648"
---
# <a name="sendemail-macro-action"></a><span data-ttu-id="2b739-102">Ação da macro EnviarEmail</span><span class="sxs-lookup"><span data-stu-id="2b739-102">SendEmail macro action</span></span>

<span data-ttu-id="2b739-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2b739-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2b739-104">A ação **EnviarEmail** envia uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="2b739-104">The **SendEmail** action sends an email message.</span></span>

> [!NOTE]
> <span data-ttu-id="2b739-105">A ação **EnviarEmail** está disponível somente em Macros de Dados.</span><span class="sxs-lookup"><span data-stu-id="2b739-105">The **SendEmail** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="2b739-106">Configuração</span><span class="sxs-lookup"><span data-stu-id="2b739-106">Setting</span></span>

<span data-ttu-id="2b739-107">A ação **EnviarEmail** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="2b739-107">The **SendEmail** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2b739-108">Argument</span><span class="sxs-lookup"><span data-stu-id="2b739-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="2b739-109">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="2b739-109">Required</span></span></p></th>
<th><p><span data-ttu-id="2b739-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="2b739-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b739-111"><strong>To</strong></span><span class="sxs-lookup"><span data-stu-id="2b739-111"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="2b739-112">Sim</span><span class="sxs-lookup"><span data-stu-id="2b739-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="2b739-113">Os destinatários da mensagem cujos nomes você deseja colocar na linha <strong>para</strong> da mensagem. Separe os nomes de destinatários especificados neste argumento (e nos argumentos <em>CC</em> e <em>Cco</em> ) com ponto e vírgula (;).</span><span class="sxs-lookup"><span data-stu-id="2b739-113">The recipients of the message whose names you want to put on the <strong>To</strong> line in the message.Separate the recipient names that you specify in this argument (and in the <em>Cc</em> and <em>Bcc</em> arguments) with a semicolon (;).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b739-114"><strong>Cc</strong></span><span class="sxs-lookup"><span data-stu-id="2b739-114"><strong>Cc</strong></span></span></p></td>
<td><p><span data-ttu-id="2b739-115">Não</span><span class="sxs-lookup"><span data-stu-id="2b739-115">No</span></span></p></td>
<td><p><span data-ttu-id="2b739-116">Os destinatários da mensagem cujos nomes você deseja colocar na linha CC (&quot;cópia&quot;carbono) na mensagem.</span><span class="sxs-lookup"><span data-stu-id="2b739-116">The message recipients whose names you want to put on the Cc (&quot;carbon copy&quot;) line in the message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b739-117"><strong>Bcc</strong></span><span class="sxs-lookup"><span data-stu-id="2b739-117"><strong>Bcc</strong></span></span></p></td>
<td><p><span data-ttu-id="2b739-118">Não</span><span class="sxs-lookup"><span data-stu-id="2b739-118">No</span></span></p></td>
<td><p><span data-ttu-id="2b739-119">Os destinatários da mensagem cujos nomes você deseja colocar na linha Cco (&quot;com cópia&quot;oculta) da mensagem.</span><span class="sxs-lookup"><span data-stu-id="2b739-119">The message recipients whose names you want to put on the Bcc (&quot;blind carbon copy&quot;) line in the message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b739-120"><strong>Subject</strong></span><span class="sxs-lookup"><span data-stu-id="2b739-120"><strong>Subject</strong></span></span></p></td>
<td><p><span data-ttu-id="2b739-121">Não</span><span class="sxs-lookup"><span data-stu-id="2b739-121">No</span></span></p></td>
<td><p><span data-ttu-id="2b739-p101">O assunto da mensagem. Esse texto aparece na linha <strong>Assunto</strong> da mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="2b739-p101">The subject of the message. This text appears on the <strong>Subject</strong> line in the message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b739-124"><strong>Body</strong></span><span class="sxs-lookup"><span data-stu-id="2b739-124"><strong>Body</strong></span></span></p></td>
<td><p><span data-ttu-id="2b739-125">Não</span><span class="sxs-lookup"><span data-stu-id="2b739-125">No</span></span></p></td>
<td><p><span data-ttu-id="2b739-p102">O texto que você deseja incluir no corpo principal da mensagem de email. Se você deixar esse argumento em branco, nenhum texto adicional será incluído na mensagem.</span><span class="sxs-lookup"><span data-stu-id="2b739-p102">The text that you want to include in the main body of the mail message. If you leave this argument blank, no additional text is included in the message.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2b739-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="2b739-128">Remarks</span></span>

<span data-ttu-id="2b739-129">A ação **EnviarEmail** está disponível somente nos eventos de macro **[Após Exclusão](after-delete-macro-event.md)**, **[Após Inserir](after-insert-macro-event.md)** e **[Após Atualizar](after-update-macro-event.md)**.</span><span class="sxs-lookup"><span data-stu-id="2b739-129">The **SendEmail** action is available only in the **[After Delete](after-delete-macro-event.md)**, **[After Insert](after-insert-macro-event.md)**, and **[After Update](after-update-macro-event.md)** macro events.</span></span>

<span data-ttu-id="2b739-130">A ação **EnviarEmail** não exibe a mensagem para edição.</span><span class="sxs-lookup"><span data-stu-id="2b739-130">The **SendEmail** action does not display the message for editing.</span></span>

