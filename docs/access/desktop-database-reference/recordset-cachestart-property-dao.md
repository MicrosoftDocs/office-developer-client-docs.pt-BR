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
ms.openlocfilehash: 44981d8c19f76ee0a1d6df5fbdaeb72b35357336
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886932"
---
# <a name="recordsetcachestart-property-dao"></a><span data-ttu-id="1482b-102">Propriedade Recordset.CacheStart (DAO)</span><span class="sxs-lookup"><span data-stu-id="1482b-102">Recordset.CacheStart Property (DAO)</span></span>


<span data-ttu-id="1482b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="1482b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1482b-104">Define ou retorna um valor que especifica o indicador do primeiro registro em um objeto Recordset tipo dynaset contendo dados para serem armazenados em cache localmente a partir da fonte de dados ODBC (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="1482b-104">Sets or returns a value that specifies the bookmark of the first record in a dynaset-type Recordset object containing data to be locally cached from an ODBC data source (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="1482b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1482b-105">Syntax</span></span>

<span data-ttu-id="1482b-106">*expressão* . CacheStart</span><span class="sxs-lookup"><span data-stu-id="1482b-106">*expression* .CacheStart</span></span>

<span data-ttu-id="1482b-107">*expressão* Uma variável que representa um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="1482b-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1482b-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="1482b-108">Remarks</span></span>

<span data-ttu-id="1482b-p101">Dados armazenados em cache melhoram o desempenho se você usa objetos **Recordset** para recuperar dados de um servidor remoto. Um cache é um espaço na memória local que mantém os dados mais recentemente recuperados do servidor; isso é útil quando os usuários solicitam esses dados novamente durante a execução de um aplicativo. Quando os usuários solicitam dados, o mecanismo de banco de dados do Microsoft Access verifica esses dados no cache primeiro em vez de recuperá-los do servidor, o que leva mais tempo. O cache salva apenas dados provenientes de uma fonte de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="1482b-p101">Data caching improves performance if you use **Recordset** objects to retrieve data from a remote server. A cache is a space in local memory that holds the data most recently retrieved from the server; this is useful if users request the data again while the application is running. When users request data, the Microsoft Access database engine checks the cache for the requested data first rather than retrieving it from the server, which takes more time. The cache only saves data that comes from an ODBC data source.</span></span>

<span data-ttu-id="1482b-p102">Qualquer fonte de dados ODBC conectada ao mecanismo de banco de dados do Microsoft Access, como uma tabela vinculada, pode ter um cache local. Para criar o cache, abra um objeto **Recordset** a partir da fonte de dados remota, defina as propriedades **CacheSize** e **[CacheStart](recordset-cachestart-property-dao.md)** e utilize o método **[FillCache](recordset-fillcache-method-dao.md)** ou navegue pelos registros utilizando os métodos **Move**.</span><span class="sxs-lookup"><span data-stu-id="1482b-p102">Any Microsoft Access database engine-connected ODBC data source, such as a linked table, can have a local cache. To create the cache, open a **Recordset** object from the remote data source, set the **CacheSize** and **[CacheStart](recordset-cachestart-property-dao.md)** properties, and then use the **[FillCache](recordset-fillcache-method-dao.md)** method, or step through the records by using the **Move** methods.</span></span>

<span data-ttu-id="1482b-p103">A configuração da propriedade **CacheStart** é o indicador do primeiro registro no objeto **Recordset** a ser armazenado em cache. Você pode usar o indicador de qualquer registro para definir a propriedade **CacheStart**. Torne o registro que deve iniciar o cache o registro atual e defina a propriedade **CacheStart** igual à propriedade **[Bookmark](recordset-bookmark-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="1482b-p103">The **CacheStart** property setting is the bookmark of the first record in the **Recordset** object to be cached. You can use the bookmark of any record to set the **CacheStart** property. Make the record you want to start the cache the current record, and set the **CacheStart** property equal to the **[Bookmark](recordset-bookmark-property-dao.md)** property.</span></span>

<span data-ttu-id="1482b-118">O mecanismo de banco de dados do Microsoft Access solicita os registros dentro do intervalo de cache, a partir do cache, e solicita os registros fora do intervalo de cache a partir do servidor.</span><span class="sxs-lookup"><span data-stu-id="1482b-118">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="1482b-119">Os registros recuperados do cache não refletem as alterações feitas simultaneamente por outros usuários na fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="1482b-119">Records retrieved from the cache don't reflect changes made concurrently to the source data by other users.</span></span>

<span data-ttu-id="1482b-120">Para forçar uma atualização de todos os dados em cache, defina a propriedade **CacheSize** do objeto **Recordset** como 0, redefina-a para o tamanho do cache solicitado originalmente e use o método **FillCache**.</span><span class="sxs-lookup"><span data-stu-id="1482b-120">To force an update of all the cached data, set the **CacheSize** property of the **Recordset** object to 0, re-set it to the size of the cache you originally requested, and then use the **FillCache** method.</span></span>

