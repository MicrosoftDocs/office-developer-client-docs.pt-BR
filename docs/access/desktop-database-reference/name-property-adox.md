---
title: Propriedade Name (ADOX)
TOCTitle: Name Property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4ea92fcca60d0c2877bf89359aac4532356a9874
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604047"
---
# <a name="name-property-adox"></a><span data-ttu-id="7e1a0-102">Propriedade Name (ADOX)</span><span class="sxs-lookup"><span data-stu-id="7e1a0-102">Name Property (ADOX)</span></span>


<span data-ttu-id="7e1a0-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7e1a0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7e1a0-104">Indica o nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="7e1a0-104">Indicates the name of the object.</span></span>

<span data-ttu-id="7e1a0-105"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="7e1a0-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="7e1a0-106">Configurações e valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7e1a0-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="7e1a0-107">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="7e1a0-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="7e1a0-108">mestre</span><span class="sxs-lookup"><span data-stu-id="7e1a0-108">master</span></span>

<span data-ttu-id="7e1a0-109">Define ou retorna um valor **String**.</span><span class="sxs-lookup"><span data-stu-id="7e1a0-109">Sets or returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e1a0-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="7e1a0-110">Remarks</span></span>

<span data-ttu-id="7e1a0-111">Os nomes não precisam ser exclusivos em uma coleção.</span><span class="sxs-lookup"><span data-stu-id="7e1a0-111">Names do not have to be unique within a collection.</span></span>

<span data-ttu-id="7e1a0-p101">A propriedade **Name** é de leitura/gravação nos objetos [Column](column-object-adox.md), [Group](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md) e [User](user-object-adox.md). A propriedade **Name** é somente leitura nos objetos [Catalog](catalog-object-adox.md), [Procedure](procedure-object-adox.md) e [View](view-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="7e1a0-p101">The **Name** property is read/write on [Column](column-object-adox.md), [Group](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md), and [User](user-object-adox.md) objects. The **Name** property is read-only on [Catalog](catalog-object-adox.md), [Procedure](procedure-object-adox.md), and [View](view-object-adox.md) objects.</span></span>

<span data-ttu-id="7e1a0-114">No caso de objetos de leitura/gravação (**Column**, **Group**, **Key**, **Index**, **Table** e **User**), o valor padrão é uma sequência de caracteres vazia ("").</span><span class="sxs-lookup"><span data-stu-id="7e1a0-114">For read/write objects (**Column**, **Group**, **Key**, **Index**, **Table** and **User** objects), the default value is an empty string ("").</span></span>


> [!NOTE]
> <P><span data-ttu-id="7e1a0-115">[!OBSERVAçãO] No caso de chaves, esta propriedade é somente leitura em objetos <STRONG>Key</STRONG> já acrescentados a uma coleção.</span><span class="sxs-lookup"><span data-stu-id="7e1a0-115">For keys, this property is read-only on <STRONG>Key</STRONG> objects already appended to a collection.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="7e1a0-116">[!OBSERVAçãO] No caso de tabelas, essa propriedade é somente leitura em objetos <STRONG>Table</STRONG> já acrescentados a uma coleção.</span><span class="sxs-lookup"><span data-stu-id="7e1a0-116">For tables, this property is read-only for <STRONG>Table</STRONG> objects already appended to a collection.</span></span></P>


