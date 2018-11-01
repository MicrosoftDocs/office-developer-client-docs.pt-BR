---
title: Propriedade DataSource (ADO)
TOCTitle: DataSource property (ADO)
ms:assetid: 5c5d6c9b-b7d4-45a5-0f6a-a5580a74361e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249325(v=office.15)
ms:contentKeyID: 48545087
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a6b889deb9ccf713c2313b207387be8f6b1681b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868158"
---
# <a name="datasource-property-ado"></a><span data-ttu-id="bab17-102">Propriedade DataSource (ADO)</span><span class="sxs-lookup"><span data-stu-id="bab17-102">DataSource property (ADO)</span></span>


<span data-ttu-id="bab17-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="bab17-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bab17-104">Indica um objeto que contém dados a serem representados como um objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="bab17-104">Indicates an object that contains data to be represented as a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bab17-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="bab17-105">Remarks</span></span>

<span data-ttu-id="bab17-p101">Essa propriedade é usada para criar controles vinculados a dados no Ambiente de Dados. O Ambiente de Dados mantém as coleções de dados (fontes de dados) contendo objetos nomeados (*membros de dados*) que serão representados como um objeto \**Recordset\*\*\*.*</span><span class="sxs-lookup"><span data-stu-id="bab17-p101">This property is used to create data-bound controls with the Data Environment. The Data Environment maintains collections of data (data sources) containing named objects (*data members*) that will be represented as a **Recordset** object *.*</span></span>

<span data-ttu-id="bab17-108">As propriedades [DataMember](datamember-property-ado.md) e **DataSource** devem ser usadas em conjunto.</span><span class="sxs-lookup"><span data-stu-id="bab17-108">The [DataMember](datamember-property-ado.md) and **DataSource** properties must be used in conjunction.</span></span>

<span data-ttu-id="bab17-109">O objeto referido deve implementar a interface **IDataSource** e deve conter uma interface **IRowset**.</span><span class="sxs-lookup"><span data-stu-id="bab17-109">The object referenced must implement the **IDataSource** interface and must contain an **IRowset** interface.</span></span>

<span data-ttu-id="bab17-110">**Uso**</span><span class="sxs-lookup"><span data-stu-id="bab17-110">**Usage**</span></span>

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
