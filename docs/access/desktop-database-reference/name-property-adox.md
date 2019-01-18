---
title: Propriedade Name (ADOX)
TOCTitle: Name property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5c7021c6f97d1aaa9c82e65eab98a3259d6eb87e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707980"
---
# <a name="name-property-adox"></a><span data-ttu-id="f3bab-102">Propriedade Name (ADOX)</span><span class="sxs-lookup"><span data-stu-id="f3bab-102">Name property (ADOX)</span></span>

<span data-ttu-id="f3bab-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="f3bab-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f3bab-104">Indica o nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="f3bab-104">Indicates the name of the object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="f3bab-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="f3bab-105">Settings and return values</span></span>

<span data-ttu-id="f3bab-106">Define ou retorna um valor **String**.</span><span class="sxs-lookup"><span data-stu-id="f3bab-106">Sets or returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3bab-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="f3bab-107">Remarks</span></span>

<span data-ttu-id="f3bab-108">Os nomes não precisam ser exclusivos em uma coleção.</span><span class="sxs-lookup"><span data-stu-id="f3bab-108">Names do not have to be unique within a collection.</span></span>

<span data-ttu-id="f3bab-p101">A propriedade **Name** é de leitura/gravação nos objetos [Column](column-object-adox.md), [Group](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md) e [User](user-object-adox.md). A propriedade **Name** é somente leitura nos objetos [Catalog](catalog-object-adox.md), [Procedure](procedure-object-adox.md) e [View](view-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="f3bab-p101">The **Name** property is read/write on [Column](column-object-adox.md), [Group](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md), and [User](user-object-adox.md) objects. The **Name** property is read-only on [Catalog](catalog-object-adox.md), [Procedure](procedure-object-adox.md), and [View](view-object-adox.md) objects.</span></span>

<span data-ttu-id="f3bab-111">No caso de objetos de leitura/gravação (**Column**, **Group**, **Key**, **Index**, **Table** e **User**), o valor padrão é uma sequência de caracteres vazia ("").</span><span class="sxs-lookup"><span data-stu-id="f3bab-111">For read/write objects (**Column**, **Group**, **Key**, **Index**, **Table** and **User** objects), the default value is an empty string ("").</span></span>

> [!NOTE]
> - <span data-ttu-id="f3bab-112">[!OBSERVAçãO] No caso de chaves, esta propriedade é somente leitura em objetos **Key** já acrescentados a uma coleção.</span><span class="sxs-lookup"><span data-stu-id="f3bab-112">For keys, this property is read-only on **Key** objects already appended to a collection.</span></span>
> - <span data-ttu-id="f3bab-113">[!OBSERVAçãO] No caso de tabelas, essa propriedade é somente leitura em objetos **Table** já acrescentados a uma coleção.</span><span class="sxs-lookup"><span data-stu-id="f3bab-113">For tables, this property is read-only for **Table** objects already appended to a collection.</span></span>


