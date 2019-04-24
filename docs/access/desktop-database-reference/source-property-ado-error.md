---
title: Propriedade Source (Error do ADO)
TOCTitle: Source property (ADO Error)
ms:assetid: ffc6c77f-1494-d63a-d832-416faa4c6f07
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250316(v=office.15)
ms:contentKeyID: 48548969
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2f03dcc8049113df13ff8654aee340d1e2d6e502
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308593"
---
# <a name="source-property-ado-error"></a><span data-ttu-id="2c10f-102">Propriedade Source (Error do ADO)</span><span class="sxs-lookup"><span data-stu-id="2c10f-102">Source property (ADO Error)</span></span>


<span data-ttu-id="2c10f-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2c10f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2c10f-104">Indica o nome do objeto ou aplicativo que gerou originalmente um erro.</span><span class="sxs-lookup"><span data-stu-id="2c10f-104">Indicates the name of the object or application that originally generated an error.</span></span>

## <a name="return-value"></a><span data-ttu-id="2c10f-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2c10f-105">Return value</span></span>

<span data-ttu-id="2c10f-106">Retorna um valor **String** que indica o nome de um objeto ou aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2c10f-106">Returns a **String** value that indicates the name of an object or application.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c10f-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c10f-107">Remarks</span></span>

<span data-ttu-id="2c10f-108">Use a propriedade **Source** em um objeto [Error](error-object-ado.md) para determinar o nome do objeto ou aplicativo que gerou originalmente um erro.</span><span class="sxs-lookup"><span data-stu-id="2c10f-108">Use the **Source** property on an [Error](error-object-ado.md) object to determine the name of the object or application that originally generated an error.</span></span> <span data-ttu-id="2c10f-109">Pode ser o nome da classe do objeto ou um identificador programático.</span><span class="sxs-lookup"><span data-stu-id="2c10f-109">This could be the object's class name or programmatic ID.</span></span> <span data-ttu-id="2c10f-110">Para erros no ADO, o valor da propriedade será \**ADODB. \* \* \* ObjectName*, onde *objectname* é o nome do objeto que disparou o erro.</span><span class="sxs-lookup"><span data-stu-id="2c10f-110">For errors in ADO, the property value will be \**ADODB.\*\*\*ObjectName*, where *ObjectName* is the name of the object that triggered the error.</span></span> <span data-ttu-id="2c10f-111">Para o ADOX e o ADO MD, o valor será \**ADOX. \* \* "ObjectName* e \**ADOMD. \* \* \* ObjectName,* respectivamente.</span><span class="sxs-lookup"><span data-stu-id="2c10f-111">For ADOX and ADO MD, the value will be \**ADOX.\*\*\*ObjectName* and \**ADOMD.\*\*\*ObjectName,* respectively.</span></span>

<span data-ttu-id="2c10f-112">Com base na documentação de erros das propriedades **Source**, [Number](number-property-ado.md) e [Description](description-property-ado.md) de objetos **Error**, você pode escrever um código que trate o erro apropriadamente.</span><span class="sxs-lookup"><span data-stu-id="2c10f-112">Based on the error documentation from the **Source**, [Number](number-property-ado.md), and [Description](description-property-ado.md) properties of **Error** objects, you can write code that will handle the error appropriately.</span></span>

<span data-ttu-id="2c10f-113">A propriedade **Source** é somente leitura para objetos **Error**.</span><span class="sxs-lookup"><span data-stu-id="2c10f-113">The **Source** property is read-only for **Error** objects.</span></span>

