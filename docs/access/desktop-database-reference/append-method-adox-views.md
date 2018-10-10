---
title: Método Append (Modos de exibição do ADOX)
TOCTitle: Append Method (ADOX Views)
ms:assetid: 202f1d0a-dc5d-84e5-daf3-3212e5bc6088
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248985(v=office.15)
ms:contentKeyID: 48543655
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 106dd9d72cb350422f00da05859bc096cb2b52e9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463700"
---
# <a name="append-method-adox-views"></a><span data-ttu-id="a3c00-102">Método Append (Modos de exibição do ADOX)</span><span class="sxs-lookup"><span data-stu-id="a3c00-102">Append Method (ADOX Views)</span></span>


<span data-ttu-id="a3c00-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a3c00-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="a3c00-104">Cria e anexa um novo objeto [View](view-object-adox.md) à coleção [Views](views-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="a3c00-104">Creates a new [View](view-object-adox.md) object and appends it to the [Views](views-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3c00-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3c00-105">Syntax</span></span>

<span data-ttu-id="a3c00-106">*Modos de exibição*. Acrescentar o*nome*, *comando*</span><span class="sxs-lookup"><span data-stu-id="a3c00-106">*Views*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="a3c00-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3c00-107">Parameters</span></span>

  - <span data-ttu-id="a3c00-108">*Name*</span><span class="sxs-lookup"><span data-stu-id="a3c00-108">*Name*</span></span>

  - <span data-ttu-id="a3c00-109">Um valor **String** que especifica o nome do modo de exibição a ser criado.</span><span class="sxs-lookup"><span data-stu-id="a3c00-109">A **String** value that specifies the name of the view to create.</span></span>

  - <span data-ttu-id="a3c00-110">*Command*</span><span class="sxs-lookup"><span data-stu-id="a3c00-110">*Command*</span></span>

  - <span data-ttu-id="a3c00-111">Um objeto [Command](command-object-ado.md) do ADO que representa o modo de exibição a ser criado.</span><span class="sxs-lookup"><span data-stu-id="a3c00-111">An ADO [Command](command-object-ado.md) object that represents the view to create.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3c00-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="a3c00-112">Remarks</span></span>

<span data-ttu-id="a3c00-113">Cria um novo modo de exibição na fonte de dados, com o nome e os atributos especificados no objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="a3c00-113">Creates a new view in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="a3c00-p101">Se o texto do comando que o usuário especificar representar um procedimento em vez de um modo de exibição, o comportamento dependerá do provedor. O comando **Append** irá falhar se o provedor não oferecer suporte para comandos persistentes.</span><span class="sxs-lookup"><span data-stu-id="a3c00-p101">If the command text that the user specifies represents a procedure rather than a view, the behavior is dependent upon the provider. **Append** will fail if the provider does not support persisting commands.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a3c00-116">Ao usar o OLE DB Provider for Microsoft Jet, a método <STRONG>Append</STRONG> da coleção <STRONG>Views</STRONG> permitirá que você especifique um <STRONG>procedimento</STRONG> em vez de um <STRONG>modo de exibição</STRONG> no parâmetro <EM>comando</EM> .</span><span class="sxs-lookup"><span data-stu-id="a3c00-116">When using the OLE DB Provider for Microsoft Jet, the <STRONG>Views</STRONG> collection <STRONG>Append</STRONG> method will allow you to specify a <STRONG>Procedure</STRONG> rather than a <STRONG>View</STRONG> in the <EM>Command</EM> parameter.</span></span> <span data-ttu-id="a3c00-117">O <STRONG>Procedimento</STRONG> será adicionado à fonte de dados e será adicionado à coleção <STRONG>Views</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="a3c00-117">The <STRONG>Procedure</STRONG> will be added to the data source and will be added to the <STRONG>Views</STRONG> collection.</span></span> <span data-ttu-id="a3c00-118">Após o comando <STRONG>Append</STRONG>, se as coleções <STRONG>Procedures</STRONG> e <STRONG>Views</STRONG> forem atualizadas, o <STRONG>Procedimento</STRONG> não estará mais na coleção <STRONG>Views</STRONG> e será exibido na coleção <STRONG>Procedures</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="a3c00-118">After the <STRONG>Append</STRONG>, if the <STRONG>Procedures</STRONG> and <STRONG>Views</STRONG> collections are refreshed, the <STRONG>Procedure</STRONG> will no longer be in the <STRONG>Views</STRONG> collection and will appear in the <STRONG>Procedures</STRONG> collection.</span></span></P>


