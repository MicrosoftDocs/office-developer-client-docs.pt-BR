---
title: Propriedade Value (ADO)
TOCTitle: Value property (ADO)
ms:assetid: ff21d122-98e3-2b48-d92f-e696b8079fc5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250310(v=office.15)
ms:contentKeyID: 48548958
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 00b82706d934356621ac1e41fffca61ec88e081f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715064"
---
# <a name="value-property-ado"></a><span data-ttu-id="26a62-102">Propriedade Value (ADO)</span><span class="sxs-lookup"><span data-stu-id="26a62-102">Value property (ADO)</span></span>

<span data-ttu-id="26a62-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="26a62-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="26a62-104">Indica o valor atribuído a um objeto [Field](field-object-ado.md), [Parameter](parameter-object-ado.md) ou [Property](property-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="26a62-104">Indicates the value assigned to a [Field](field-object-ado.md), [Parameter](parameter-object-ado.md), or [Property](property-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="26a62-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="26a62-105">Settings and return values</span></span>

<span data-ttu-id="26a62-p101">Define ou retorna um valor **Variant** que indica o valor do objeto. O valor padrão depende da propriedade [Type](type-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="26a62-p101">Sets or returns a **Variant** value that indicates the value of the object. Default value depends on the [Type](type-property-ado.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="26a62-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="26a62-108">Remarks</span></span>

<span data-ttu-id="26a62-p102">Utilize a propriedade **Value** para definir ou retornar dados a partir dos objetos **Field**, para definir ou retornar valores de parâmetro com os objetos **Parameter**, ou para definir ou retornar definições de propriedade com os objetos **Property**. A definição da propriedade **Value** como leitura/gravação ou somente leitura depende de diversos fatores  consulte os tópicos do respectivo objeto para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="26a62-p102">Use the **Value** property to set or return data from **Field** objects, to set or return parameter values with **Parameter** objects, or to set or return property settings with **Property** objects. Whether the **Value** property is read/write or read-only depends upon numerous factors — see the respective object topics for more information.</span></span>

<span data-ttu-id="26a62-111">O ADO permite a definição e o retorno de dados binários longos com a propriedade **Value**.</span><span class="sxs-lookup"><span data-stu-id="26a62-111">ADO allows setting and returning long binary data with the **Value** property.</span></span>

> [!NOTE]
> <span data-ttu-id="26a62-p103">[!OBSERVAçãO] Para os objetos **Parameter**, o ADO lê a propriedade **Value** somente uma vez a partir do provedor. Se um comando contiver um **Parameter** cuja propriedade **Value** esteja vazia e você criar um [Recordset](recordset-object-ado.md) a partir do comando, certifique-se de fechar o **Recordset** antes de recuperar a propriedade **Value**. Caso contrário, para alguns provedores, a propriedade **Value** poderá ficar vazia e não conterá o valor correto.</span><span class="sxs-lookup"><span data-stu-id="26a62-p103">For **Parameter** objects, ADO reads the **Value** property only once from the provider. If a command contains a **Parameter** whose **Value** property is empty, and you create a [Recordset](recordset-object-ado.md) from the command, ensure that you first close the **Recordset** before retrieving the **Value** property. Otherwise, for some providers, the **Value** property may be empty, and won't contain the correct value.</span></span>

<span data-ttu-id="26a62-p104">Para novos objetos **Field** que foram acrescentados à coleção [Fields](fields-collection-ado.md) de um objeto [Record](record-object-ado.md), a propriedade **Value** deverá ser definida antes que qualquer outra propriedade **Field** seja especificada. Primeiro, um valor específico para a propriedade **Value** deve ser atribuído e o método [Update](update-method-ado.md) deve ser chamado na coleção **Fields**. Assim, outras propriedades, como [Type](type-property-ado.md) ou [Attributes](attributes-property-ado.md), poderão ser acessadas.</span><span class="sxs-lookup"><span data-stu-id="26a62-p104">For new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md) object, the **Value** property must be set before any other **Field** properties can be specified. First, a specific value for the **Value** property must have been assigned and [Update](update-method-ado.md) on the **Fields** collection called. Then, other properties such as [Type](type-property-ado.md) or [Attributes](attributes-property-ado.md) can be accessed.</span></span>

