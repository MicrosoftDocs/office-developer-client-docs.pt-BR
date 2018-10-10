---
title: Método Append (Procedimentos do ADOX)
TOCTitle: Append Method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5c1afc7aeea90fc152df7d8f7b1601bf3753b3a3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462319"
---
# <a name="append-method-adox-procedures"></a><span data-ttu-id="314f0-102">Método Append (Procedimentos do ADOX)</span><span class="sxs-lookup"><span data-stu-id="314f0-102">Append Method (ADOX Procedures)</span></span>


<span data-ttu-id="314f0-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="314f0-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="314f0-104">Adiciona um novo objeto [Procedure](procedure-object-adox.md) à coleção [Procedures](procedures-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="314f0-104">Adds a new [Procedure](procedure-object-adox.md) object to the [Procedures](procedures-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="314f0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="314f0-105">Syntax</span></span>

<span data-ttu-id="314f0-106">*Procedimentos*. Acrescentar o*nome*, *comando*</span><span class="sxs-lookup"><span data-stu-id="314f0-106">*Procedures*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="314f0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="314f0-107">Parameters</span></span>

  - <span data-ttu-id="314f0-108">*Name*</span><span class="sxs-lookup"><span data-stu-id="314f0-108">*Name*</span></span>

  - <span data-ttu-id="314f0-109">Um valor **String** que especifica o nome do procedimento a ser criado e anexado.</span><span class="sxs-lookup"><span data-stu-id="314f0-109">A **String** value that specifies the name of the procedure to create and append.</span></span>

  - <span data-ttu-id="314f0-110">*Command*</span><span class="sxs-lookup"><span data-stu-id="314f0-110">*Command*</span></span>

  - <span data-ttu-id="314f0-111">Um objeto [Command](command-object-ado.md) do ADO que representa o procedimento a ser criado e anexado.</span><span class="sxs-lookup"><span data-stu-id="314f0-111">An ADO [Command](command-object-ado.md) object that represents the procedure to create and append.</span></span>

## <a name="remarks"></a><span data-ttu-id="314f0-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="314f0-112">Remarks</span></span>

<span data-ttu-id="314f0-113">Cria um novo procedimento na fonte de dados, com o nome e os atributos especificados no objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="314f0-113">Creates a new procedure in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="314f0-p101">Se o texto do comando que o usuário especificar representar um modo de exibição em vez de um procedimento, o comportamento dependerá do provedor que estiver sendo usado. O comando **Append** irá falhar se o provedor não oferecer suporte para comandos persistentes.</span><span class="sxs-lookup"><span data-stu-id="314f0-p101">If the command text that the user specifies represents a view rather than a procedure, the behavior is dependent upon the provider being used. **Append** will fail if the provider does not support persisting commands.</span></span>


> [!NOTE]
> <P><span data-ttu-id="314f0-116">Ao usar o OLE DB Provider for Microsoft Jet, o método <STRONG>Append</STRONG> da coleção <STRONG>Procedures</STRONG> permitirá que você especifique um <STRONG>modo de exibição</STRONG> em vez de um <STRONG>procedimento</STRONG> no parâmetro <EM>comando</EM> .</span><span class="sxs-lookup"><span data-stu-id="314f0-116">When using the OLE DB Provider for Microsoft Jet, the <STRONG>Procedures</STRONG> collection <STRONG>Append</STRONG> method will allow you to specify a <STRONG>View</STRONG> rather than a <STRONG>Procedure</STRONG> in the <EM>Command</EM> parameter.</span></span> <span data-ttu-id="314f0-117">O <STRONG>Modo de exibição</STRONG> será adicionado à fonte de dados e será adicionado à coleção <STRONG>Procedures</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="314f0-117">The <STRONG>View</STRONG> will be added to the data source and will be added to the <STRONG>Procedures</STRONG> collection.</span></span> <span data-ttu-id="314f0-118">Após o comando <STRONG>Append</STRONG>, se as coleções <STRONG>Procedures</STRONG> e <STRONG>Views</STRONG> forem atualizadas, o <STRONG>Modo de exibição</STRONG> não estará mais na coleção <STRONG>Procedures</STRONG> e será exibido na coleção <STRONG>Views</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="314f0-118">After the <STRONG>Append</STRONG>, if the <STRONG>Procedures</STRONG> and <STRONG>Views</STRONG> collections are refreshed, the <STRONG>View</STRONG> will no longer be in the <STRONG>Procedures</STRONG> collection and will appear in the <STRONG>Views</STRONG> collection.</span></span></P>


