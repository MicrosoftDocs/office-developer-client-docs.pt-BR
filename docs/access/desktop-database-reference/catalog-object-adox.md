---
title: Objeto Catalog (ADOX)
TOCTitle: Catalog object (ADOX)
ms:assetid: d9e8d94b-9161-3eb6-abaf-00d1244d1f2d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250097(v=office.15)
ms:contentKeyID: 48548068
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8cc0237d1419c3aba818d54811f1dbdeeaa441c3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28714903"
---
# <a name="catalog-object-adox"></a><span data-ttu-id="345db-102">Objeto Catalog (ADOX)</span><span class="sxs-lookup"><span data-stu-id="345db-102">Catalog object (ADOX)</span></span>


<span data-ttu-id="345db-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="345db-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="345db-104">Contém coleções ([Tables](tables-collection-adox.md), [Views](views-collection-adox.md), [Users](users-collection-adox.md), [Groups](groups-collection-adox.md) e [Procedures](procedures-collection-adox.md)) que descrevem o catálogo de esquemas de uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="345db-104">Contains collections ([Tables](tables-collection-adox.md), [Views](views-collection-adox.md), [Users](users-collection-adox.md), [Groups](groups-collection-adox.md), and [Procedures](procedures-collection-adox.md)) that describe the schema catalog of a data source.</span></span>

## <a name="remarks"></a><span data-ttu-id="345db-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="345db-105">Remarks</span></span>

<span data-ttu-id="345db-p101">Você pode modificar o objeto **Catalog** adicionando ou removendo objetos ou modificando objetos existentes. Alguns provedores podem não oferecer suporte para todos os objetos **Catalog** ou podem oferecer suporte apenas para a exibição de informações do esquema.</span><span class="sxs-lookup"><span data-stu-id="345db-p101">You can modify the **Catalog** object by adding or removing objects or by modifying existing objects. Some providers may not support all of the **Catalog** objects or may support only viewing schema information.</span></span>

<span data-ttu-id="345db-108">Com as propriedades e métodos de um objeto **Catalog**, você pode:</span><span class="sxs-lookup"><span data-stu-id="345db-108">With the properties and methods of a **Catalog** object, you can:</span></span>

- <span data-ttu-id="345db-109">Abrir o catálogo definindo a propriedade [ActiveConnection](activeconnection-property-adox.md) para um objeto [Connection](connection-object-ado.md) do ADO ou para uma sequência de conexão válida.</span><span class="sxs-lookup"><span data-stu-id="345db-109">Open the catalog by setting the [ActiveConnection](activeconnection-property-adox.md) property to an ADO [Connection](connection-object-ado.md) object or a valid connection string.</span></span>

- <span data-ttu-id="345db-110">Criar um novo catálogo com o método [Create](create-method-adox.md).</span><span class="sxs-lookup"><span data-stu-id="345db-110">Create a new catalog with the [Create](create-method-adox.md) method.</span></span>

- <span data-ttu-id="345db-111">Determinar os proprietários dos objetos em um **Catálogo** com os métodos [GetObjectOwner](getobjectowner-method-adox.md) e [SetObjectOwner](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/setobjectowner-method-adox).</span><span class="sxs-lookup"><span data-stu-id="345db-111">Determine the owners of the objects in a **Catalog** with the [GetObjectOwner](getobjectowner-method-adox.md) and [SetObjectOwner](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/setobjectowner-method-adox) methods.</span></span>

