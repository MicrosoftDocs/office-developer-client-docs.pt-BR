---
title: Método Append (Procedimentos do ADOX)
TOCTitle: Append method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a2de9dc7d8dccfc4107dbd802c4013ac794acf61
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704844"
---
# <a name="append-method-adox-procedures"></a><span data-ttu-id="ba8a1-102">Método Append (Procedimentos do ADOX)</span><span class="sxs-lookup"><span data-stu-id="ba8a1-102">Append method (ADOX Procedures)</span></span>

<span data-ttu-id="ba8a1-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="ba8a1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ba8a1-104">Adiciona um novo objeto [Procedure](procedure-object-adox.md) à coleção [Procedures](procedures-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="ba8a1-104">Adds a new [Procedure](procedure-object-adox.md) object to the [Procedures](procedures-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba8a1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba8a1-105">Syntax</span></span>

<span data-ttu-id="ba8a1-106">*Procedimentos*. Acrescentar o*nome*, *comando*</span><span class="sxs-lookup"><span data-stu-id="ba8a1-106">*Procedures*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="ba8a1-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba8a1-107">Parameters</span></span>

|<span data-ttu-id="ba8a1-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="ba8a1-108">Parameter</span></span>|<span data-ttu-id="ba8a1-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="ba8a1-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="ba8a1-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="ba8a1-110">*Name*</span></span> |<span data-ttu-id="ba8a1-111">Um valor **String** que especifica o nome do procedimento a ser criado e anexado.</span><span class="sxs-lookup"><span data-stu-id="ba8a1-111">A **String** value that specifies the name of the procedure to create and append.</span></span>|
|<span data-ttu-id="ba8a1-112">*Command*</span><span class="sxs-lookup"><span data-stu-id="ba8a1-112">*Command*</span></span> |<span data-ttu-id="ba8a1-113">Um objeto [Command](command-object-ado.md) do ADO que representa o procedimento a ser criado e anexado.</span><span class="sxs-lookup"><span data-stu-id="ba8a1-113">An ADO [Command](command-object-ado.md) object that represents the procedure to create and append.</span></span>|

## <a name="remarks"></a><span data-ttu-id="ba8a1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba8a1-114">Remarks</span></span>

<span data-ttu-id="ba8a1-115">Cria um novo procedimento na fonte de dados, com o nome e os atributos especificados no objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="ba8a1-115">Creates a new procedure in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="ba8a1-p101">Se o texto do comando que o usuário especificar representar um modo de exibição em vez de um procedimento, o comportamento dependerá do provedor que estiver sendo usado. O comando **Append** irá falhar se o provedor não oferecer suporte para comandos persistentes.</span><span class="sxs-lookup"><span data-stu-id="ba8a1-p101">If the command text that the user specifies represents a view rather than a procedure, the behavior is dependent upon the provider being used. **Append** will fail if the provider does not support persisting commands.</span></span>

> [!NOTE]
> <span data-ttu-id="ba8a1-118">Ao usar o OLE DB Provider for Microsoft Jet, o método **Append** da coleção **Procedures** permitirá que você especifique um **modo de exibição** em vez de um **procedimento** no parâmetro *comando* .</span><span class="sxs-lookup"><span data-stu-id="ba8a1-118">When using the OLE DB Provider for Microsoft Jet, the **Procedures** collection **Append** method will allow you to specify a **View** rather than a **Procedure** in the *Command* parameter.</span></span> <span data-ttu-id="ba8a1-119">O **Modo de exibição** será adicionado à fonte de dados e será adicionado à coleção **Procedures**.</span><span class="sxs-lookup"><span data-stu-id="ba8a1-119">The **View** will be added to the data source and will be added to the **Procedures** collection.</span></span> <span data-ttu-id="ba8a1-120">Após o comando **Append**, se as coleções **Procedures** e **Views** forem atualizadas, o **Modo de exibição** não estará mais na coleção **Procedures** e será exibido na coleção **Views**.</span><span class="sxs-lookup"><span data-stu-id="ba8a1-120">After the **Append**, if the **Procedures** and **Views** collections are refreshed, the **View** will no longer be in the **Procedures** collection and will appear in the **Views** collection.</span></span>


