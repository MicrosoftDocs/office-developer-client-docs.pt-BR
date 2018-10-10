---
title: Propriedade Name (ADOX)
TOCTitle: Name Property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 51ea68718c7605df03ed8e4d44d4cb48011649fd
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462244"
---
# <a name="name-property-adox"></a><span data-ttu-id="90ce9-102">Propriedade Name (ADOX)</span><span class="sxs-lookup"><span data-stu-id="90ce9-102">Name Property (ADOX)</span></span>


<span data-ttu-id="90ce9-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="90ce9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="90ce9-104">Indica o nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="90ce9-104">Indicates the name of the object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="90ce9-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="90ce9-105">Settings and Return Values</span></span>

<span data-ttu-id="90ce9-106">Define ou retorna um valor **String**.</span><span class="sxs-lookup"><span data-stu-id="90ce9-106">Sets or returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="90ce9-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="90ce9-107">Remarks</span></span>

<span data-ttu-id="90ce9-108">Os nomes não precisam ser exclusivos em uma coleção.</span><span class="sxs-lookup"><span data-stu-id="90ce9-108">Names do not have to be unique within a collection.</span></span>

<span data-ttu-id="90ce9-p101">A propriedade **Name** é de leitura/gravação nos objetos [Column](column-object-adox.md), [Group](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md) e [User](user-object-adox.md). A propriedade **Name** é somente leitura nos objetos [Catalog](catalog-object-adox.md), [Procedure](procedure-object-adox.md) e [View](view-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="90ce9-p101">The **Name** property is read/write on [Column](column-object-adox.md), [Group](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md), and [User](user-object-adox.md) objects. The **Name** property is read-only on [Catalog](catalog-object-adox.md), [Procedure](procedure-object-adox.md), and [View](view-object-adox.md) objects.</span></span>

<span data-ttu-id="90ce9-111">No caso de objetos de leitura/gravação (**Column**, **Group**, **Key**, **Index**, **Table** e **User**), o valor padrão é uma sequência de caracteres vazia ("").</span><span class="sxs-lookup"><span data-stu-id="90ce9-111">For read/write objects (**Column**, **Group**, **Key**, **Index**, **Table** and **User** objects), the default value is an empty string ("").</span></span>


> [!NOTE]
> <P><span data-ttu-id="90ce9-112">[!OBSERVAçãO] No caso de chaves, esta propriedade é somente leitura em objetos <STRONG>Key</STRONG> já acrescentados a uma coleção.</span><span class="sxs-lookup"><span data-stu-id="90ce9-112">For keys, this property is read-only on <STRONG>Key</STRONG> objects already appended to a collection.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="90ce9-113">[!OBSERVAçãO] No caso de tabelas, essa propriedade é somente leitura em objetos <STRONG>Table</STRONG> já acrescentados a uma coleção.</span><span class="sxs-lookup"><span data-stu-id="90ce9-113">For tables, this property is read-only for <STRONG>Table</STRONG> objects already appended to a collection.</span></span></P>


