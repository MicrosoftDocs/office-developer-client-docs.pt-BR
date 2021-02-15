---
title: Propriedade Recordset.CacheStart (DAO)
TOCTitle: CacheStart Property
ms:assetid: 03814312-660a-d8e9-8a7b-bc14d66e05ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844802(v=office.15)
ms:contentKeyID: 48542986
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053171
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 514f109f0eed902287e519bcd7a729397e70eaa5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300613"
---
# <a name="recordsetcachestart-property-dao"></a><span data-ttu-id="f91c8-102">Propriedade Recordset.CacheStart (DAO)</span><span class="sxs-lookup"><span data-stu-id="f91c8-102">Recordset.CacheStart property (DAO)</span></span>


<span data-ttu-id="f91c8-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f91c8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f91c8-104">Define ou retorna um valor que especifica o marcador do primeiro registro em um objeto Recordset do tipo dynaset, que contém os dados a serem armazenados localmente a partir de uma fonte de dados ODBC (somente em espaços de trabalho do Microsoft Access ).</span><span class="sxs-lookup"><span data-stu-id="f91c8-104">Sets or returns a value that specifies the bookmark of the first record in a dynaset-type Recordset object containing data to be locally cached from an ODBC data source (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="f91c8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f91c8-105">Syntax</span></span>

<span data-ttu-id="f91c8-106">*expressão* . CacheStart</span><span class="sxs-lookup"><span data-stu-id="f91c8-106">*expression* .CacheStart</span></span>

<span data-ttu-id="f91c8-107">*expression* Uma variável que representa um objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f91c8-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f91c8-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="f91c8-108">Remarks</span></span>

<span data-ttu-id="f91c8-p101">O cache de dados melhorará o desempenho, se você usar os objetos **Recordset** para recuperar dados de um servidor remoto. Um cache é um espaço na memória local que mantém os dados recuperados do servidor mais recentemente; isso será útil se os usuários solicitarem os dados novamente enquanto o aplicativo estiver em execução. Quando os usuários solicitarem os dados, o mecanismo do banco de dados do Microsoft Access verificará o cache dos dados solicitados primeiro em vez de recuperá-los do servidor, o que levará mais tempo. O cache salvará apenas os dados provenientes de uma fonte de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="f91c8-p101">Data caching improves performance if you use **Recordset** objects to retrieve data from a remote server. A cache is a space in local memory that holds the data most recently retrieved from the server; this is useful if users request the data again while the application is running. When users request data, the Microsoft Access database engine checks the cache for the requested data first rather than retrieving it from the server, which takes more time. The cache only saves data that comes from an ODBC data source.</span></span>

<span data-ttu-id="f91c8-p102">Qualquer mecanismo de banco de dados do Microsoft Access conectado à fonte de dados ODBC, como uma tabela vinculada, pode ter um cache local. Para criar o cache, abra um objeto **Recordset** a partir da fonte de dados remota, defina as propriedades **CacheSize** e **[CacheStart](recordset-cachestart-property-dao.md)** e depois use o método **[FillCache](recordset-fillcache-method-dao.md)** ou consulte por etapas os registros usando os métodos **Move**.</span><span class="sxs-lookup"><span data-stu-id="f91c8-p102">Any Microsoft Access database engine-connected ODBC data source, such as a linked table, can have a local cache. To create the cache, open a **Recordset** object from the remote data source, set the **CacheSize** and **[CacheStart](recordset-cachestart-property-dao.md)** properties, and then use the **[FillCache](recordset-fillcache-method-dao.md)** method, or step through the records by using the **Move** methods.</span></span>

<span data-ttu-id="f91c8-p103">A definição da propriedade **CacheStart** é o marcador do primeiro registro no objeto **Recordset** a ser armazenado. Use o marcador de um registro para definir a propriedade **CacheStart**. Faça o registro que quiser para iniciar o cache do período atual e defina a propriedade **CacheStart** como igual à propriedade **[Bookmark](recordset-bookmark-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="f91c8-p103">The **CacheStart** property setting is the bookmark of the first record in the **Recordset** object to be cached. You can use the bookmark of any record to set the **CacheStart** property. Make the record you want to start the cache the current record, and set the **CacheStart** property equal to the **[Bookmark](recordset-bookmark-property-dao.md)** property.</span></span>

<span data-ttu-id="f91c8-118">O mecanismo do banco de dados do Microsoft Access solicita registros em um intervalo de cache a partir do cache e requisita registros de fora do intervalo de cache a partir do servidor.</span><span class="sxs-lookup"><span data-stu-id="f91c8-118">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="f91c8-119">Os registros recuperados do cache não refletem as alterações feitas de forma simultânea com os dados da fonte de outros usuários.</span><span class="sxs-lookup"><span data-stu-id="f91c8-119">Records retrieved from the cache don't reflect changes made concurrently to the source data by other users.</span></span>

<span data-ttu-id="f91c8-120">Para forçar uma atualização em todos os dados armazenados, defina a propriedade **CacheSize** do objeto **Recordset** como 0, redefina-o para o tamanho de cache solicitado originalmente e depois use o método **FillCache**.</span><span class="sxs-lookup"><span data-stu-id="f91c8-120">To force an update of all the cached data, set the **CacheSize** property of the **Recordset** object to 0, re-set it to the size of the cache you originally requested, and then use the **FillCache** method.</span></span>

