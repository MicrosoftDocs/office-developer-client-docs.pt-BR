---
title: Propriedade Name (ADO)
TOCTitle: Name property (ADO)
ms:assetid: 4b19bd08-ac3c-86f0-471d-06a37a0d4f89
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249234(v=office.15)
ms:contentKeyID: 48544683
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f6fbfbd7008919cc4d784a4d0468d8471d102708
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288662"
---
# <a name="name-property-ado"></a><span data-ttu-id="1ba91-102">Propriedade Name (ADO)</span><span class="sxs-lookup"><span data-stu-id="1ba91-102">Name property (ADO)</span></span>


<span data-ttu-id="1ba91-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1ba91-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1ba91-104">Indica o nome de um objeto</span><span class="sxs-lookup"><span data-stu-id="1ba91-104">Indicates the name of an object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="1ba91-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="1ba91-105">Settings and return values</span></span>

<span data-ttu-id="1ba91-106">Define ou retorna um valor **String** que indica o nome de um objeto.</span><span class="sxs-lookup"><span data-stu-id="1ba91-106">Sets or returns a **String** value that indicates the name of an object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ba91-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ba91-107">Remarks</span></span>

<span data-ttu-id="1ba91-108">Use a propriedade **Name** para atribuir um nome ou recuperar o nome de um objeto **Command**, **Property**, **Field** ou **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="1ba91-108">Use the **Name** property to assign a name to or retrieve the name of a **Command**, **Property**, **Field**, or **Parameter** object.</span></span>

<span data-ttu-id="1ba91-109">O valor é leitura/gravação em um objeto **Command** e somente leitura em um objeto **Property**.</span><span class="sxs-lookup"><span data-stu-id="1ba91-109">The value is read/write on a **Command** object and read-only on a **Property** object.</span></span>

<span data-ttu-id="1ba91-p101">Para um objeto **Field**, **Name** normalmente é somente leitura. No entanto, para novos objetos **Field** que foram acrescentados à coleção [Fields](fields-collection-ado.md) de um [Record](record-object-ado.md), **Name** será leitura/gravação apenas depois que a propriedade [Value](value-property-ado.md) para **Field** for especificada e o provedor de dados adicionar com sucesso o novo **Field** chamando o método [Update](update-method-ado.md) da coleção **Fields**.</span><span class="sxs-lookup"><span data-stu-id="1ba91-p101">For a **Field** object, **Name** is normally read-only. However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Name** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="1ba91-p102">Para os objetos **Parameter** que ainda não foram acrescentados à coleção [Parameters](parameters-collection-ado.md), a propriedade **Name** é leitura/gravação. Para objetos **Parameter** acrescentados e todos os outros objetos, a propriedade **Name** é somente leitura. Os nomes não precisam ser exclusivos em uma coleção.</span><span class="sxs-lookup"><span data-stu-id="1ba91-p102">For **Parameter** objects not yet appended to the [Parameters](parameters-collection-ado.md) collection, the **Name** property is read/write. For appended **Parameter** objects and all other objects, the **Name** property is read-only. Names do not have to be unique within a collection.</span></span>

<span data-ttu-id="1ba91-115">Você pode recuperar a propriedade **Name** de um objeto por uma referência ordinal, após a qual pode se referir ao objeto diretamente pelo nome.</span><span class="sxs-lookup"><span data-stu-id="1ba91-115">You can retrieve the **Name** property of an object by an ordinal reference, after which you can refer to the object directly by name.</span></span> <span data-ttu-id="1ba91-116">Por exemplo, se rstMain. Properties (20). O nome produz a capacidade de atualização, posteriormente, você pode referir-se a essa propriedade como produz a capacidade de atualização, em seguida, pode referir-se a essa propriedade como rstMain. Properties ("atualização").</span><span class="sxs-lookup"><span data-stu-id="1ba91-116">For example, if rstMain.Properties(20).Name yields Updatability , you can subsequently refer to this property as yields Updatability , you can subsequently refer to this property as rstMain.Properties("Updatability") .</span></span>

