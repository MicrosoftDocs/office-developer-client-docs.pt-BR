---
title: Propriedade DataSource (ADO)
TOCTitle: DataSource property (ADO)
ms:assetid: 5c5d6c9b-b7d4-45a5-0f6a-a5580a74361e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249325(v=office.15)
ms:contentKeyID: 48545087
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0dec30715d1eb4e31d7490db4cedd015ecf3c040
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700028"
---
# <a name="datasource-property-ado"></a><span data-ttu-id="b25c9-102">Propriedade DataSource (ADO)</span><span class="sxs-lookup"><span data-stu-id="b25c9-102">DataSource property (ADO)</span></span>


<span data-ttu-id="b25c9-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="b25c9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b25c9-104">Indica um objeto que contém dados a serem representados como um objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="b25c9-104">Indicates an object that contains data to be represented as a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b25c9-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="b25c9-105">Remarks</span></span>

<span data-ttu-id="b25c9-p101">Essa propriedade é usada para criar controles vinculados a dados no Ambiente de Dados. O Ambiente de Dados mantém as coleções de dados (fontes de dados) contendo objetos nomeados (*membros de dados*) que serão representados como um objeto \**Recordset\*\*\*.*</span><span class="sxs-lookup"><span data-stu-id="b25c9-p101">This property is used to create data-bound controls with the Data Environment. The Data Environment maintains collections of data (data sources) containing named objects (*data members*) that will be represented as a **Recordset** object *.*</span></span>

<span data-ttu-id="b25c9-108">As propriedades [DataMember](datamember-property-ado.md) e **DataSource** devem ser usadas em conjunto.</span><span class="sxs-lookup"><span data-stu-id="b25c9-108">The [DataMember](datamember-property-ado.md) and **DataSource** properties must be used in conjunction.</span></span>

<span data-ttu-id="b25c9-109">O objeto referido deve implementar a interface **IDataSource** e deve conter uma interface **IRowset**.</span><span class="sxs-lookup"><span data-stu-id="b25c9-109">The object referenced must implement the **IDataSource** interface and must contain an **IRowset** interface.</span></span>

<span data-ttu-id="b25c9-110">**Uso**</span><span class="sxs-lookup"><span data-stu-id="b25c9-110">**Usage**</span></span>

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
