---
title: Método Append (Modos de exibição do ADOX)
TOCTitle: Append method (ADOX Views)
ms:assetid: 202f1d0a-dc5d-84e5-daf3-3212e5bc6088
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248985(v=office.15)
ms:contentKeyID: 48543655
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9e1a6e14542f267af6a9f5bc58bb2d75a11aac77
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716149"
---
# <a name="append-method-adox-views"></a><span data-ttu-id="7f191-102">Método Append (Modos de exibição do ADOX)</span><span class="sxs-lookup"><span data-stu-id="7f191-102">Append method (ADOX Views)</span></span>

<span data-ttu-id="7f191-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="7f191-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7f191-104">Cria e anexa um novo objeto [View](view-object-adox.md) à coleção [Views](views-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="7f191-104">Creates a new [View](view-object-adox.md) object and appends it to the [Views](views-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f191-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7f191-105">Syntax</span></span>

<span data-ttu-id="7f191-106">*Modos de exibição*. Acrescentar o*nome*, *comando*</span><span class="sxs-lookup"><span data-stu-id="7f191-106">*Views*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="7f191-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7f191-107">Parameters</span></span>

|<span data-ttu-id="7f191-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="7f191-108">Parameter</span></span>|<span data-ttu-id="7f191-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="7f191-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="7f191-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="7f191-110">*Name*</span></span> |<span data-ttu-id="7f191-111">Um valor **String** que especifica o nome do modo de exibição a ser criado.</span><span class="sxs-lookup"><span data-stu-id="7f191-111">A **String** value that specifies the name of the view to create.</span></span>|
|<span data-ttu-id="7f191-112">*Command*</span><span class="sxs-lookup"><span data-stu-id="7f191-112">*Command*</span></span> |<span data-ttu-id="7f191-113">Um objeto [Command](command-object-ado.md) do ADO que representa o modo de exibição a ser criado.</span><span class="sxs-lookup"><span data-stu-id="7f191-113">An ADO [Command](command-object-ado.md) object that represents the view to create.</span></span>|

## <a name="remarks"></a><span data-ttu-id="7f191-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f191-114">Remarks</span></span>

<span data-ttu-id="7f191-115">Cria um novo modo de exibição na fonte de dados, com o nome e os atributos especificados no objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="7f191-115">Creates a new view in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="7f191-p101">Se o texto do comando que o usuário especificar representar um procedimento em vez de um modo de exibição, o comportamento dependerá do provedor. O comando **Append** irá falhar se o provedor não oferecer suporte para comandos persistentes.</span><span class="sxs-lookup"><span data-stu-id="7f191-p101">If the command text that the user specifies represents a procedure rather than a view, the behavior is dependent upon the provider. **Append** will fail if the provider does not support persisting commands.</span></span>

> [!NOTE]
> <span data-ttu-id="7f191-118">Ao usar o OLE DB Provider for Microsoft Jet, a método **Append** da coleção **Views** permitirá que você especifique um **procedimento** em vez de um **modo de exibição** no parâmetro *comando* .</span><span class="sxs-lookup"><span data-stu-id="7f191-118">When using the OLE DB Provider for Microsoft Jet, the **Views** collection **Append** method will allow you to specify a **Procedure** rather than a **View** in the *Command* parameter.</span></span> <span data-ttu-id="7f191-119">O **Procedimento** será adicionado à fonte de dados e será adicionado à coleção **Views**.</span><span class="sxs-lookup"><span data-stu-id="7f191-119">The **Procedure** will be added to the data source and will be added to the **Views** collection.</span></span> <span data-ttu-id="7f191-120">Após o comando **Append**, se as coleções **Procedures** e **Views** forem atualizadas, o **Procedimento** não estará mais na coleção **Views** e será exibido na coleção **Procedures**.</span><span class="sxs-lookup"><span data-stu-id="7f191-120">After the **Append**, if the **Procedures** and **Views** collections are refreshed, the **Procedure** will no longer be in the **Views** collection and will appear in the **Procedures** collection.</span></span>


