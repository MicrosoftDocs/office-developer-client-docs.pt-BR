---
title: Propriedade ParentCatalog (ADOX)
TOCTitle: ParentCatalog property (ADOX)
ms:assetid: 7eef4ef5-1fa4-73ea-a710-fc8767c9ea21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249535(v=office.15)
ms:contentKeyID: 48545891
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d7a10bac3c02a771518038351bc4d0b780c0e774
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707455"
---
# <a name="parentcatalog-property-adox"></a><span data-ttu-id="3254d-102">Propriedade ParentCatalog (ADOX)</span><span class="sxs-lookup"><span data-stu-id="3254d-102">ParentCatalog property (ADOX)</span></span>


<span data-ttu-id="3254d-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="3254d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3254d-104">Especifica o catálogo pai de um tabela ou coluna para conceder acesso a propriedades específicas do provedor.</span><span class="sxs-lookup"><span data-stu-id="3254d-104">Specifies the parent catalog of a table or column to provide access to provider-specific properties.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="3254d-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="3254d-105">Settings and return values</span></span>

<span data-ttu-id="3254d-p101">Define e retorna um objeto [Catalog](catalog-object-adox.md). A definição de **ParentCatalog** como um objeto **Catalog** aberto permite acessar propriedades específicas do provedor antes de acrescentar uma tabela ou coluna a uma coleção **Catalog**.</span><span class="sxs-lookup"><span data-stu-id="3254d-p101">Sets and returns a [Catalog](catalog-object-adox.md) object. Setting **ParentCatalog** to an open **Catalog** allows access to provider-specific properties prior to appending a table or column to a **Catalog** collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="3254d-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="3254d-108">Remarks</span></span>

<span data-ttu-id="3254d-p102">Alguns provedores de dados permitem que valores de propriedade específicos do provedor sejam gravados somente na fase de criação (quando uma tabela ou coluna é acrescentada à sua coleção **Catalog** ). Para acessar essas propriedades antes de acrescentar esses objetos a um **Catalog**, especifique primeiro o objeto **Catalog** na propriedade **ParentCatalog**.</span><span class="sxs-lookup"><span data-stu-id="3254d-p102">Some data providers allow provider-specific property values to be written only at creation (when a table or column is appended to its **Catalog** collection). To access these properties before appending these objects to a **Catalog**, specify the **Catalog** in the **ParentCatalog** property first.</span></span>

<span data-ttu-id="3254d-111">Ocorre um erro quando a tabela ou coluna é acrescentada a um objeto **Catalog** que não seja **ParentCatalog**.</span><span class="sxs-lookup"><span data-stu-id="3254d-111">An error occurs when the table or column is appended to a different **Catalog** than the **ParentCatalog**.</span></span>

