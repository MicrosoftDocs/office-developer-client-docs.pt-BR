---
title: Método Create (ADOX)
TOCTitle: Create Method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cffaa8fb924d2fd272300c77fc5a9c3dc0b239db
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464774"
---
# <a name="create-method-adox"></a><span data-ttu-id="41e07-102">Método Create (ADOX)</span><span class="sxs-lookup"><span data-stu-id="41e07-102">Create Method (ADOX)</span></span>


<span data-ttu-id="41e07-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="41e07-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="41e07-104">Cria um novo catálogo.</span><span class="sxs-lookup"><span data-stu-id="41e07-104">Creates a new catalog.</span></span>

## <a name="syntax"></a><span data-ttu-id="41e07-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="41e07-105">Syntax</span></span>

<span data-ttu-id="41e07-106">*Catálogo*. Criar*ConnectString*</span><span class="sxs-lookup"><span data-stu-id="41e07-106">*Catalog*.Create*ConnectString*</span></span>

## <a name="parameters"></a><span data-ttu-id="41e07-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="41e07-107">Parameters</span></span>

  - <span data-ttu-id="41e07-108">*ConnectString*</span><span class="sxs-lookup"><span data-stu-id="41e07-108">*ConnectString*</span></span>

  - <span data-ttu-id="41e07-109">Um valor **String** usado para estabelecer conexão com a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="41e07-109">A **String** value used to connect to the data source.</span></span>

## <a name="remarks"></a><span data-ttu-id="41e07-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="41e07-110">Remarks</span></span>

<span data-ttu-id="41e07-p101">O método **Create** cria e abre uma nova [Conexão](connection-object-ado.md) do ADO com a fonte de dados especificada em *ConnectString*. Se for bem-sucedido, o novo objeto **Connection** será atribuído à propriedade [ActiveConnection](activeconnection-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="41e07-p101">The **Create** method creates and opens a new ADO [Connection](connection-object-ado.md) to the data source specified in *ConnectString*. If successful, the new **Connection** object is assigned to the [ActiveConnection](activeconnection-property-adox.md) property.</span></span>

<span data-ttu-id="41e07-113">Ocorrerá um erro se o provedor não oferecer suporte para a criação de novos catálogos.</span><span class="sxs-lookup"><span data-stu-id="41e07-113">An error will occur if the provider does not support creating new catalogs.</span></span>

