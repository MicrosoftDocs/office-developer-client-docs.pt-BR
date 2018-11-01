---
title: Método Append (Procedimentos do ADOX)
TOCTitle: Append Method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ef11c9d45cc5b34b5ef7b1cf762dfd6f3e4c1d64
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873044"
---
# <a name="append-method-adox-procedures"></a><span data-ttu-id="bc01a-102">Método Append (Procedimentos do ADOX)</span><span class="sxs-lookup"><span data-stu-id="bc01a-102">Append Method (ADOX Procedures)</span></span>


<span data-ttu-id="bc01a-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="bc01a-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="bc01a-104">Adiciona um novo objeto [Procedure](procedure-object-adox.md) à coleção [Procedures](procedures-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="bc01a-104">Adds a new [Procedure](procedure-object-adox.md) object to the [Procedures](procedures-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc01a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bc01a-105">Syntax</span></span>

<span data-ttu-id="bc01a-106">*Procedimentos*. Acrescentar o*nome*, *comando*</span><span class="sxs-lookup"><span data-stu-id="bc01a-106">*Procedures*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="bc01a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc01a-107">Parameters</span></span>

  - <span data-ttu-id="bc01a-108">*Name*</span><span class="sxs-lookup"><span data-stu-id="bc01a-108">*Name*</span></span>

  - <span data-ttu-id="bc01a-109">Um valor **String** que especifica o nome do procedimento a ser criado e anexado.</span><span class="sxs-lookup"><span data-stu-id="bc01a-109">A **String** value that specifies the name of the procedure to create and append.</span></span>

  - <span data-ttu-id="bc01a-110">*Command*</span><span class="sxs-lookup"><span data-stu-id="bc01a-110">*Command*</span></span>

  - <span data-ttu-id="bc01a-111">Um objeto [Command](command-object-ado.md) do ADO que representa o procedimento a ser criado e anexado.</span><span class="sxs-lookup"><span data-stu-id="bc01a-111">An ADO [Command](command-object-ado.md) object that represents the procedure to create and append.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc01a-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc01a-112">Remarks</span></span>

<span data-ttu-id="bc01a-113">Cria um novo procedimento na fonte de dados, com o nome e os atributos especificados no objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="bc01a-113">Creates a new procedure in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="bc01a-p101">Se o texto do comando que o usuário especificar representar um modo de exibição em vez de um procedimento, o comportamento dependerá do provedor que estiver sendo usado. O comando **Append** irá falhar se o provedor não oferecer suporte para comandos persistentes.</span><span class="sxs-lookup"><span data-stu-id="bc01a-p101">If the command text that the user specifies represents a view rather than a procedure, the behavior is dependent upon the provider being used. **Append** will fail if the provider does not support persisting commands.</span></span>


> [!NOTE]
> <span data-ttu-id="bc01a-116">Ao usar o OLE DB Provider for Microsoft Jet, o método **Append** da coleção **Procedures** permitirá que você especifique um **modo de exibição** em vez de um **procedimento** no parâmetro *comando* .</span><span class="sxs-lookup"><span data-stu-id="bc01a-116">When using the OLE DB Provider for Microsoft Jet, the **Procedures** collection **Append** method will allow you to specify a **View** rather than a **Procedure** in the *Command* parameter.</span></span> <span data-ttu-id="bc01a-117">O **Modo de exibição** será adicionado à fonte de dados e será adicionado à coleção **Procedures**.</span><span class="sxs-lookup"><span data-stu-id="bc01a-117">The **View** will be added to the data source and will be added to the **Procedures** collection.</span></span> <span data-ttu-id="bc01a-118">Após o comando **Append**, se as coleções **Procedures** e **Views** forem atualizadas, o **Modo de exibição** não estará mais na coleção **Procedures** e será exibido na coleção **Views**.</span><span class="sxs-lookup"><span data-stu-id="bc01a-118">After the **Append**, if the **Procedures** and **Views** collections are refreshed, the **View** will no longer be in the **Procedures** collection and will appear in the **Views** collection.</span></span>


