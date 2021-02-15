---
title: Propriedade Size (ADO)
TOCTitle: Size property (ADO)
ms:assetid: 24596b5c-b1cc-e97e-68b6-8ff53baf150b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249017(v=office.15)
ms:contentKeyID: 48543753
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2a1bed3454d081b9d5de3a01e9b326130b40baa4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306927"
---
# <a name="size-property-ado"></a><span data-ttu-id="6af7d-102">Propriedade Size (ADO)</span><span class="sxs-lookup"><span data-stu-id="6af7d-102">Size property (ADO)</span></span>


<span data-ttu-id="6af7d-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6af7d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6af7d-104">Indica o tamanho máximo, em bytes ou caracteres, de um objeto [Parameter](parameter-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="6af7d-104">Indicates the maximum size, in bytes or characters, of a [Parameter](parameter-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="6af7d-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="6af7d-105">Settings and return values</span></span>

<span data-ttu-id="6af7d-106">Define ou retorna um valor **Long** que indica o tamanho máximo em bytes ou caracteres de um valor em um objeto **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="6af7d-106">Sets or returns a **Long** value that indicates the maximum size in bytes or characters of a value in a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6af7d-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="6af7d-107">Remarks</span></span>

<span data-ttu-id="6af7d-108">Utilize a propriedade **Size** para determinar o tamanho máximo dos valores gravados em ou lidos a partir da propriedade [Value](value-property-ado.md) de um objeto **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="6af7d-108">Use the **Size** property to determine the maximum size for values written to or read from the [Value](value-property-ado.md) property of a **Parameter** object.</span></span>

<span data-ttu-id="6af7d-109">Se você especificar um tipo de dados de tamanho variável para um objeto **Parameter** (por exemplo, qualquer tipo **String**, como **adVarChar**), será preciso definir a propriedade **Size** do objeto antes de acrescentá-lo à coleção [Parameters](parameters-collection-ado.md); caso contrário, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="6af7d-109">If you specify a variable-length data type for a **Parameter** object (for example, any **String** type, such as **adVarChar**), you must set the object's **Size** property before appending it to the [Parameters](parameters-collection-ado.md) collection; otherwise, an error occurs.</span></span>

<span data-ttu-id="6af7d-110">Se você já tiver acrescentado o objeto **Parameter** à coleção **Parameters** de um objeto [Command](command-object-ado.md) e você alterar seu tipo para um tipo de dados de tamanho variável, será preciso definir a propriedade **Size** do objeto **Parameter** antes de executar o objeto **Command**; caso contrário, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="6af7d-110">If you have already appended the **Parameter** object to the **Parameters** collection of a [Command](command-object-ado.md) object and you change its type to a variable-length data type, you must set the **Parameter** object's **Size** property before executing the **Command** object; otherwise, an error occurs.</span></span>

<span data-ttu-id="6af7d-p101">Se você utilizar o método [Refresh](refresh-method-ado.md) para obter as informações de parâmetro a partir de um provedor e ele retornar um ou mais objetos **Parameter** de tipo de dados de tamanho variável, o ADO poderá alocar memória para os parâmetros com base em seu potencial máximo de tamanho, o que poderia causar um erro durante a execução. Para evitar um erro, você deve definir explicitamente a propriedade **Size** para esses parâmetros antes de executar o comando.</span><span class="sxs-lookup"><span data-stu-id="6af7d-p101">If you use the [Refresh](refresh-method-ado.md) method to obtain parameter information from the provider and it returns one or more variable-length data type **Parameter** objects, ADO may allocate memory for the parameters based on their maximum potential size, which could cause an error during execution. To prevent an error, you should explicitly set the **Size** property for these parameters before executing the command.</span></span>

<span data-ttu-id="6af7d-113">A propriedade **Size** é leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="6af7d-113">The **Size** property is read/write.</span></span>

