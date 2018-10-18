---
title: Propriedade ParentCatalog (ADOX)
TOCTitle: ParentCatalog Property (ADOX)
ms:assetid: 7eef4ef5-1fa4-73ea-a710-fc8767c9ea21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249535(v=office.15)
ms:contentKeyID: 48545891
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d9fdd4b41578b4f185d199a47204faabd0af3ff8
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603410"
---
# <a name="parentcatalog-property-adox"></a><span data-ttu-id="102be-102">Propriedade ParentCatalog (ADOX)</span><span class="sxs-lookup"><span data-stu-id="102be-102">ParentCatalog Property (ADOX)</span></span>


<span data-ttu-id="102be-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="102be-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="102be-104">Especifica o catálogo pai de um tabela ou coluna para conceder acesso a propriedades específicas do provedor.</span><span class="sxs-lookup"><span data-stu-id="102be-104">Specifies the parent catalog of a table or column to provide access to provider-specific properties.</span></span>

<span data-ttu-id="102be-105"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="102be-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="102be-106">Configurações e valor de retorno</span><span class="sxs-lookup"><span data-stu-id="102be-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="102be-107">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="102be-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="102be-108">mestre</span><span class="sxs-lookup"><span data-stu-id="102be-108">master</span></span>

<span data-ttu-id="102be-p101">Define e retorna um objeto [Catalog](catalog-object-adox.md). A definição de **ParentCatalog** como um objeto **Catalog** aberto permite acessar propriedades específicas do provedor antes de acrescentar uma tabela ou coluna a uma coleção **Catalog**.</span><span class="sxs-lookup"><span data-stu-id="102be-p101">Sets and returns a [Catalog](catalog-object-adox.md) object. Setting **ParentCatalog** to an open **Catalog** allows access to provider-specific properties prior to appending a table or column to a **Catalog** collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="102be-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="102be-111">Remarks</span></span>

<span data-ttu-id="102be-p102">Alguns provedores de dados permitem que valores de propriedade específicos do provedor sejam gravados somente na fase de criação (quando uma tabela ou coluna é acrescentada à sua coleção **Catalog** ). Para acessar essas propriedades antes de acrescentar esses objetos a um **Catalog**, especifique primeiro o objeto **Catalog** na propriedade **ParentCatalog**.</span><span class="sxs-lookup"><span data-stu-id="102be-p102">Some data providers allow provider-specific property values to be written only at creation (when a table or column is appended to its **Catalog** collection). To access these properties before appending these objects to a **Catalog**, specify the **Catalog** in the **ParentCatalog** property first.</span></span>

<span data-ttu-id="102be-114">Ocorre um erro quando a tabela ou coluna é acrescentada a um objeto **Catalog** que não seja **ParentCatalog**.</span><span class="sxs-lookup"><span data-stu-id="102be-114">An error occurs when the table or column is appended to a different **Catalog** than the **ParentCatalog**.</span></span>

