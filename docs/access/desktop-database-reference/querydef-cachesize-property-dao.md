---
title: Propriedade QueryDef.CacheSize (DAO)
TOCTitle: CacheSize Property
ms:assetid: a84d990e-8180-daa3-7640-47d2be8fd28b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821397(v=office.15)
ms:contentKeyID: 48546899
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1ecddf9a9972c6ded5e28748822169c2c60edc44
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462137"
---
# <a name="querydefcachesize-property-dao"></a><span data-ttu-id="7df1a-102">Propriedade QueryDef.CacheSize (DAO)</span><span class="sxs-lookup"><span data-stu-id="7df1a-102">QueryDef.CacheSize Property (DAO)</span></span>


<span data-ttu-id="7df1a-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7df1a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7df1a-p101">Define ou retorna o número de registros recuperados de uma fonte de dados ODBC que serão armazenados em cache localmente. **Long** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="7df1a-p101">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally. Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7df1a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7df1a-106">Syntax</span></span>

<span data-ttu-id="7df1a-107">*expressão* . CacheSize</span><span class="sxs-lookup"><span data-stu-id="7df1a-107">*expression* .CacheSize</span></span>

<span data-ttu-id="7df1a-108">*expressão* Uma variável que representa um objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="7df1a-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7df1a-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="7df1a-109">Remarks</span></span>

<span data-ttu-id="7df1a-p102">O valor da propriedade **CacheSize** deve estar entre 5 e 1200, mas não pode ser maior do que a memória disponível permitir. Um valor comum é 100. Uma definição de 0 desativa o armazenamento em cache.</span><span class="sxs-lookup"><span data-stu-id="7df1a-p102">The value of the **CacheSize** property must be between 5 and 1200, but not greater than available memory will allow. A typical value is 100. A setting of 0 turns off caching.</span></span>

<span data-ttu-id="7df1a-113">O mecanismo de banco de dados do Microsoft Access solicita os registros dentro do intervalo de cache, a partir do cache, e solicita os registros fora do intervalo de cache a partir do servidor.</span><span class="sxs-lookup"><span data-stu-id="7df1a-113">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="7df1a-114">Os registros recuperados do cache não refletem as alterações simultâneas que outros usuários fizeram na fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="7df1a-114">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span>

