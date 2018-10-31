---
title: Método Append (Modos de exibição do ADOX)
TOCTitle: Append Method (ADOX Views)
ms:assetid: 202f1d0a-dc5d-84e5-daf3-3212e5bc6088
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248985(v=office.15)
ms:contentKeyID: 48543655
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ca51537c78dfc07a6cd3560bba7154f6b56ef31f
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861208"
---
# <a name="append-method-adox-views"></a><span data-ttu-id="04c3b-102">Método Append (Modos de exibição do ADOX)</span><span class="sxs-lookup"><span data-stu-id="04c3b-102">Append Method (ADOX Views)</span></span>


<span data-ttu-id="04c3b-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="04c3b-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="04c3b-104">Cria e anexa um novo objeto [View](view-object-adox.md) à coleção [Views](views-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="04c3b-104">Creates a new [View](view-object-adox.md) object and appends it to the [Views](views-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="04c3b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="04c3b-105">Syntax</span></span>

<span data-ttu-id="04c3b-106">*Modos de exibição*. Acrescentar o*nome*, *comando*</span><span class="sxs-lookup"><span data-stu-id="04c3b-106">*Views*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="04c3b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="04c3b-107">Parameters</span></span>

  - <span data-ttu-id="04c3b-108">*Name*</span><span class="sxs-lookup"><span data-stu-id="04c3b-108">*Name*</span></span>

  - <span data-ttu-id="04c3b-109">Um valor **String** que especifica o nome do modo de exibição a ser criado.</span><span class="sxs-lookup"><span data-stu-id="04c3b-109">A **String** value that specifies the name of the view to create.</span></span>

  - <span data-ttu-id="04c3b-110">*Command*</span><span class="sxs-lookup"><span data-stu-id="04c3b-110">*Command*</span></span>

  - <span data-ttu-id="04c3b-111">Um objeto [Command](command-object-ado.md) do ADO que representa o modo de exibição a ser criado.</span><span class="sxs-lookup"><span data-stu-id="04c3b-111">An ADO [Command](command-object-ado.md) object that represents the view to create.</span></span>

## <a name="remarks"></a><span data-ttu-id="04c3b-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="04c3b-112">Remarks</span></span>

<span data-ttu-id="04c3b-113">Cria um novo modo de exibição na fonte de dados, com o nome e os atributos especificados no objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="04c3b-113">Creates a new view in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="04c3b-p101">Se o texto do comando que o usuário especificar representar um procedimento em vez de um modo de exibição, o comportamento dependerá do provedor. O comando **Append** irá falhar se o provedor não oferecer suporte para comandos persistentes.</span><span class="sxs-lookup"><span data-stu-id="04c3b-p101">If the command text that the user specifies represents a procedure rather than a view, the behavior is dependent upon the provider. **Append** will fail if the provider does not support persisting commands.</span></span>


> [!NOTE]
> <span data-ttu-id="04c3b-116">Ao usar o OLE DB Provider for Microsoft Jet, a método **Append** da coleção **Views** permitirá que você especifique um **procedimento** em vez de um **modo de exibição** no parâmetro *comando* .</span><span class="sxs-lookup"><span data-stu-id="04c3b-116">When using the OLE DB Provider for Microsoft Jet, the **Views** collection **Append** method will allow you to specify a **Procedure** rather than a **View** in the *Command* parameter.</span></span> <span data-ttu-id="04c3b-117">O **Procedimento** será adicionado à fonte de dados e será adicionado à coleção **Views**.</span><span class="sxs-lookup"><span data-stu-id="04c3b-117">The **Procedure** will be added to the data source and will be added to the **Views** collection.</span></span> <span data-ttu-id="04c3b-118">Após o comando **Append**, se as coleções **Procedures** e **Views** forem atualizadas, o **Procedimento** não estará mais na coleção **Views** e será exibido na coleção **Procedures**.</span><span class="sxs-lookup"><span data-stu-id="04c3b-118">After the **Append**, if the **Procedures** and **Views** collections are refreshed, the **Procedure** will no longer be in the **Views** collection and will appear in the **Procedures** collection.</span></span>


