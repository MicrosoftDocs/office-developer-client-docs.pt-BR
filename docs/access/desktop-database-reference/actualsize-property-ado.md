---
title: Propriedade ActualSize (ADO)
TOCTitle: ActualSize Property (ADO)
ms:assetid: 020a414d-e6aa-5fb9-9b77-bd9d10124f8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248787(v=office.15)
ms:contentKeyID: 48542949
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d0fa7b4f5fe27c25db51338dd1dfd1a68a936364
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25461971"
---
# <a name="actualsize-property-ado"></a><span data-ttu-id="b928a-102">Propriedade ActualSize (ADO)</span><span class="sxs-lookup"><span data-stu-id="b928a-102">ActualSize Property (ADO)</span></span>

<span data-ttu-id="b928a-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b928a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b928a-104">Indica o tamanho real do valor de um campo.</span><span class="sxs-lookup"><span data-stu-id="b928a-104">Indicates the actual length of a field's value.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="b928a-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="b928a-105">Settings and Return Values</span></span>

<span data-ttu-id="b928a-p101">Retorna um valor **Long**. Alguns provedores talvez permitam que essa propriedade seja definida para reservar espaço para dados BLOB, caso em que o valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="b928a-p101">Returns a **Long** value. Some providers may allow this property to be set to reserve space for BLOB data, in which case the default value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="b928a-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="b928a-108">Remarks</span></span>

<span data-ttu-id="b928a-p102">Use a propriedade **ActualSize** para retornar o tamanho real do valor de um objeto [Field](field-object-ado.md). Para todos os campos, a propriedade **ActualSize** é somente leitura. Se o ADO não puder determinar o tamanho do valor do objeto **Field**, a propriedade **ActualSize** retornará **adUnknown**.</span><span class="sxs-lookup"><span data-stu-id="b928a-p102">Use the **ActualSize** property to return the actual length of a [Field](field-object-ado.md) object's value. For all fields, the **ActualSize** property is read-only. If ADO cannot determine the length of the **Field** object's value, the **ActualSize** property returns **adUnknown**.</span></span>

<span data-ttu-id="b928a-p103">As propriedades **ActualSize** e [DefinedSize](definedsize-property-ado.md) são diferentes, como mostra o exemplo a seguir. Um objeto **Field** com um tipo declarado de **adVarChar** e um comprimento máximo de 50 caracteres retornará um valor de propriedade **DefinedSize** de 50, mas o valor da propriedade **ActualSize** a ser retornado será o tamanho dos dados armazenados no campo para o registro atual. **Fields** com um **DefinedSize** maior do que 255 bytes serão tratados como colunas de comprimento variável.</span><span class="sxs-lookup"><span data-stu-id="b928a-p103">The **ActualSize** and [DefinedSize](definedsize-property-ado.md) properties are different, as shown in the following example. A **Field** object with a declared type of **adVarChar** and a maximum length of 50 characters returns a **DefinedSize** property value of 50, but the **ActualSize** property value it returns is the length of the data stored in the field for the current record. **Fields** with a **DefinedSize** greater than 255 bytes are treated as variable length columns.</span></span>

