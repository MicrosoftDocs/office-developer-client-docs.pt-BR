---
title: Propriedade DataMember (ADO)
TOCTitle: DataMember property (ADO)
ms:assetid: f89e1d42-7993-764b-4e8a-2f449903f792
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250263(v=office.15)
ms:contentKeyID: 48548787
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 410f11af8daf3912dca9dc78a1cb9216ff8f8dd1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294488"
---
# <a name="datamember-property-ado"></a><span data-ttu-id="76e20-102">Propriedade DataMember (ADO)</span><span class="sxs-lookup"><span data-stu-id="76e20-102">DataMember property (ADO)</span></span>

<span data-ttu-id="76e20-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="76e20-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="76e20-104">Indica o nome do membro de dados que será recuperado do objeto referido pela propriedade [DataSource](datasource-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="76e20-104">Indicates the name of the data member that will be retrieved from the object referenced by the [DataSource](datasource-property-ado.md) property.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="76e20-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="76e20-105">Settings and return values</span></span>

<span data-ttu-id="76e20-106">Define ou retorna um valor **String**.</span><span class="sxs-lookup"><span data-stu-id="76e20-106">Sets or returns a **String** value.</span></span> <span data-ttu-id="76e20-107">O nome não diferencia maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="76e20-107">The name is not case sensitive.</span></span>

## <a name="remarks"></a><span data-ttu-id="76e20-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="76e20-108">Remarks</span></span>

<span data-ttu-id="76e20-p102">Essa propriedade é usada para criar controles vinculados a dados no Ambiente de Dados. O Ambiente de Dados mantém as coleções de dados (fontes de dados) contendo objetos nomeados (*membros de dados*) que serão representados como um objeto [Recordset](recordset-object-ado.md)*.*</span><span class="sxs-lookup"><span data-stu-id="76e20-p102">This property is used to create data-bound controls with the Data Environment. The Data Environment maintains collections of data (data sources) containing named objects (*data members*) that will be represented as a [Recordset](recordset-object-ado.md) object *.*</span></span>

<span data-ttu-id="76e20-111">As propriedades **DataMember** e **DataSource** devem ser usadas em conjunto.</span><span class="sxs-lookup"><span data-stu-id="76e20-111">The **DataMember** and **DataSource** properties must be used in conjunction.</span></span>

<span data-ttu-id="76e20-p103">A propriedade **DataMember** determina qual objeto especificado pela propriedade **DataSource** será representado como um objeto **Recordset**. O objeto **Recordset** deve ser fechado antes que essa propriedade seja definida. Ocorrerá um erro se a propriedade **DataMember** não for definida antes da propriedade **DataSource** ou se o nome do **DataMember** não for reconhecido pelo objeto especificado na propriedade **DataSource**.</span><span class="sxs-lookup"><span data-stu-id="76e20-p103">The **DataMember** property determines which object specified by the **DataSource** property will be represented as a **Recordset** object. The **Recordset** object must be closed before this property is set. An error is generated if the **DataMember** property isn't set before the **DataSource** property, or if the **DataMember** name isn't recognized by the object specified in the **DataSource** property.</span></span>

<span data-ttu-id="76e20-115">**Uso**</span><span class="sxs-lookup"><span data-stu-id="76e20-115">**Usage**</span></span>

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
