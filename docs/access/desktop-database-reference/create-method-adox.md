---
title: Método Create (ADOX)
TOCTitle: Create Method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 91f5105611df85e007dea6d0e17e3104ea5987a3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870251"
---
# <a name="create-method-adox"></a><span data-ttu-id="ff2b1-102">Método Create (ADOX)</span><span class="sxs-lookup"><span data-stu-id="ff2b1-102">Create Method (ADOX)</span></span>


<span data-ttu-id="ff2b1-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="ff2b1-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="ff2b1-104">Cria um novo catálogo.</span><span class="sxs-lookup"><span data-stu-id="ff2b1-104">Creates a new catalog.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff2b1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff2b1-105">Syntax</span></span>

<span data-ttu-id="ff2b1-106">*Catálogo*. Criar*ConnectString*</span><span class="sxs-lookup"><span data-stu-id="ff2b1-106">*Catalog*.Create*ConnectString*</span></span>

## <a name="parameters"></a><span data-ttu-id="ff2b1-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff2b1-107">Parameters</span></span>

  - <span data-ttu-id="ff2b1-108">*ConnectString*</span><span class="sxs-lookup"><span data-stu-id="ff2b1-108">*ConnectString*</span></span>

  - <span data-ttu-id="ff2b1-109">Um valor **String** usado para estabelecer conexão com a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="ff2b1-109">A **String** value used to connect to the data source.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff2b1-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff2b1-110">Remarks</span></span>

<span data-ttu-id="ff2b1-p101">O método **Create** cria e abre uma nova [Conexão](connection-object-ado.md) do ADO com a fonte de dados especificada em *ConnectString*. Se for bem-sucedido, o novo objeto **Connection** será atribuído à propriedade [ActiveConnection](activeconnection-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="ff2b1-p101">The **Create** method creates and opens a new ADO [Connection](connection-object-ado.md) to the data source specified in *ConnectString*. If successful, the new **Connection** object is assigned to the [ActiveConnection](activeconnection-property-adox.md) property.</span></span>

<span data-ttu-id="ff2b1-113">Ocorrerá um erro se o provedor não oferecer suporte para a criação de novos catálogos.</span><span class="sxs-lookup"><span data-stu-id="ff2b1-113">An error will occur if the provider does not support creating new catalogs.</span></span>

