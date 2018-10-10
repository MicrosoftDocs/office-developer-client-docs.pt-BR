---
title: Propriedade Source (Erro do ADO)
TOCTitle: Source Property (ADO Error)
ms:assetid: ffc6c77f-1494-d63a-d832-416faa4c6f07
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250316(v=office.15)
ms:contentKeyID: 48548969
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7dcc674a570b3d2adf6108316339a86333a82f9d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463556"
---
# <a name="source-property-ado-error"></a><span data-ttu-id="93e73-102">Propriedade Source (Erro do ADO)</span><span class="sxs-lookup"><span data-stu-id="93e73-102">Source Property (ADO Error)</span></span>


<span data-ttu-id="93e73-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="93e73-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="93e73-104">Indica o nome do objeto ou aplicativo que gerou originalmente um erro.</span><span class="sxs-lookup"><span data-stu-id="93e73-104">Indicates the name of the object or application that originally generated an error.</span></span>

## <a name="return-value"></a><span data-ttu-id="93e73-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="93e73-105">Return Value</span></span>

<span data-ttu-id="93e73-106">Retorna um valor **String** que indica o nome de um objeto ou aplicativo.</span><span class="sxs-lookup"><span data-stu-id="93e73-106">Returns a **String** value that indicates the name of an object or application.</span></span>

## <a name="remarks"></a><span data-ttu-id="93e73-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="93e73-107">Remarks</span></span>

<span data-ttu-id="93e73-108">Use a propriedade **Source** em um objeto [Error](error-object-ado.md) para determinar o nome do objeto ou aplicativo que gerou originalmente um erro.</span><span class="sxs-lookup"><span data-stu-id="93e73-108">Use the **Source** property on an [Error](error-object-ado.md) object to determine the name of the object or application that originally generated an error.</span></span> <span data-ttu-id="93e73-109">Pode ser o nome da classe do objeto ou um identificador programático.</span><span class="sxs-lookup"><span data-stu-id="93e73-109">This could be the object's class name or programmatic ID.</span></span> <span data-ttu-id="93e73-110">Se há erros no ADO, o valor da propriedade será \**ADODB. \* \* \* ObjectName*, onde *ObjectName* é o nome do objeto que disparou o erro.</span><span class="sxs-lookup"><span data-stu-id="93e73-110">For errors in ADO, the property value will be \**ADODB.\*\*\*ObjectName*, where *ObjectName* is the name of the object that triggered the error.</span></span> <span data-ttu-id="93e73-111">Para obter ADO MD e ADOX, o valor será \**ADOX. \* \* \* ObjectName* e \**ADOMD. \* \* \* ObjectName,* respectivamente.</span><span class="sxs-lookup"><span data-stu-id="93e73-111">For ADOX and ADO MD, the value will be \**ADOX.\*\*\*ObjectName* and \**ADOMD.\*\*\*ObjectName,* respectively.</span></span>

<span data-ttu-id="93e73-112">Com base na documentação de erros das propriedades **Source**, [Number](number-property-ado.md) e [Description](description-property-ado.md) de objetos **Error**, você pode escrever um código que trate o erro apropriadamente.</span><span class="sxs-lookup"><span data-stu-id="93e73-112">Based on the error documentation from the **Source**, [Number](number-property-ado.md), and [Description](description-property-ado.md) properties of **Error** objects, you can write code that will handle the error appropriately.</span></span>

<span data-ttu-id="93e73-113">A propriedade **Source** é somente leitura para objetos **Error**.</span><span class="sxs-lookup"><span data-stu-id="93e73-113">The **Source** property is read-only for **Error** objects.</span></span>

