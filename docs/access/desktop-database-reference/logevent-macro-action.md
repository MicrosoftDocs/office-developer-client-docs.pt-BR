---
title: Ação da macro RegistrarEvento
TOCTitle: LogEvent macro action
ms:assetid: 3578c725-64b9-385e-ef73-a15cdf751c33
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192460(v=office.15)
ms:contentKeyID: 48544148
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4106e66074975f08a5058aafbfc0c6deac156277
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715477"
---
# <a name="logevent-macro-action"></a><span data-ttu-id="588f5-102">Ação da macro RegistrarEvento</span><span class="sxs-lookup"><span data-stu-id="588f5-102">LogEvent macro action</span></span>

<span data-ttu-id="588f5-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="588f5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="588f5-104">A ação **RegistrarEvento** grava informações na tabela de sistema **USysApplicationLog**.</span><span class="sxs-lookup"><span data-stu-id="588f5-104">The **LogEvent** action writes information to the **USysApplicationLog** system table.</span></span>

> [!NOTE]
> <span data-ttu-id="588f5-105">[!OBSERVAçãO] A ação **RegistrarEvento** está disponível somente em Macros de Dados.</span><span class="sxs-lookup"><span data-stu-id="588f5-105">The **LogEvent** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="588f5-106">Configuração</span><span class="sxs-lookup"><span data-stu-id="588f5-106">Setting</span></span>

<span data-ttu-id="588f5-107">A ação **RegistrarEvento** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="588f5-107">The **LogEvent** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="588f5-108">Argumento</span><span class="sxs-lookup"><span data-stu-id="588f5-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="588f5-109">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="588f5-109">Required</span></span></p></th>
<th><p><span data-ttu-id="588f5-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="588f5-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="588f5-111"><strong>Descrição</strong></span><span class="sxs-lookup"><span data-stu-id="588f5-111"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="588f5-112">Não</span><span class="sxs-lookup"><span data-stu-id="588f5-112">No</span></span></p></td>
<td><p><span data-ttu-id="588f5-p101">Uma expressão de cadeia de caracteres que descreve a condição que você deseja registrar. A descrição não deve ultrapassar 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="588f5-p101">A string expression that describes the condition that you want to log. The description cannot exceed 255 characters.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="588f5-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="588f5-115">Remarks</span></span>

<span data-ttu-id="588f5-p102">A ação **RegistrarEvento** que pode ser usada para gravar informações de status na tabela de sistema **USysApplicationLog** sem a necessidade de usar a ação **[GerarErro](raiseerror-macro-action.md)** para exibir um erro. Por exemplo, é possível registrar alterações em um campo específico ou usar os itens gravados em **USysApplicationLog** para auxiliar na depuração da macro.</span><span class="sxs-lookup"><span data-stu-id="588f5-p102">The **LogEvent** action can be used to write status information to the **USysApplicationLog** system table that does not merit using the **[RaiseError](raiseerror-macro-action.md)** action to throw an error. For example, you could log changes to a specific field, or use the items written to the **USysApplicationLog** to assist you in debugging your macro.</span></span>

<span data-ttu-id="588f5-118">Quando você usa a ação **RegistrarEvento** para gravar na tabela **USysApplicationLog**, a coluna **Categoria** é automaticamente definida como **Usuário**.</span><span class="sxs-lookup"><span data-stu-id="588f5-118">When you use the **LogEvent** action to write to the **USysApplicationLog** table, the **Category** column is automatically set to **User**.</span></span>

<span data-ttu-id="588f5-119">Para ver a tabela **USysApplicationLog**, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="588f5-119">To see the **USysApplicationLog** table, use the following steps:</span></span>

1.  <span data-ttu-id="588f5-120">Clique no menu **Arquivo** e clique em **Opções**.</span><span class="sxs-lookup"><span data-stu-id="588f5-120">Click the **File** menu,and then click **Options**.</span></span>

2.  <span data-ttu-id="588f5-121">Na caixa de diálogo **Opções do Access**, clique na guia **Banco de Dados Atual**.</span><span class="sxs-lookup"><span data-stu-id="588f5-121">In the **Access Options** dialog box, click the **Current Database** tab.</span></span>

3.  <span data-ttu-id="588f5-122">Na seção **Navegação**, clique em **Opções de Navegação**.</span><span class="sxs-lookup"><span data-stu-id="588f5-122">In the **Navigation** section, click **Navigation Options**.</span></span>

4.  <span data-ttu-id="588f5-123">Na caixa de diálogo **Opções de Navegação**, clique em **Mostrar Objetos do Sistema** e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="588f5-123">In the **Navigation Options** dialog box, click **Show System Objects**, and then click **OK**.</span></span>

5.  <span data-ttu-id="588f5-124">Clique em **OK** para fechar a caixa de diálogo **Opções do Access**.</span><span class="sxs-lookup"><span data-stu-id="588f5-124">Click **OK** to dismiss the **Access Options** dialog box.</span></span>

