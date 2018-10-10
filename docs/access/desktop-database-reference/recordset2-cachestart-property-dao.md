---
title: Propriedade Recordset2.CacheStart (DAO)
TOCTitle: CacheStart Property
ms:assetid: 2e9c2b0d-b382-e4d6-9406-ace0e538a7b7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192239(v=office.15)
ms:contentKeyID: 48543989
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c44d70323976ade2017d406b628d3347b414f6aa
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464650"
---
# <a name="recordset2cachestart-property-dao"></a><span data-ttu-id="0cea2-102">Propriedade Recordset2.CacheStart (DAO)</span><span class="sxs-lookup"><span data-stu-id="0cea2-102">Recordset2.CacheStart Property (DAO)</span></span>


<span data-ttu-id="0cea2-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0cea2-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0cea2-104">Define ou retorna um valor que especifica o indicador do primeiro registro em um objeto Recordset tipo dynaset contendo dados para serem armazenados em cache localmente a partir da fonte de dados ODBC (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="0cea2-104">Sets or returns a value that specifies the bookmark of the first record in a dynaset-type Recordset object containing data to be locally cached from an ODBC data source (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="0cea2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0cea2-105">Syntax</span></span>

<span data-ttu-id="0cea2-106">*expressão* . CacheStart</span><span class="sxs-lookup"><span data-stu-id="0cea2-106">*expression* .CacheStart</span></span>

<span data-ttu-id="0cea2-107">*expressão* Uma variável que representa um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="0cea2-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cea2-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="0cea2-108">Remarks</span></span>

<span data-ttu-id="0cea2-p101">Dados armazenados em cache melhoram o desempenho se você usa objetos **Recordset** para recuperar dados de um servidor remoto. Um cache é um espaço na memória local que mantém os dados mais recentemente recuperados do servidor; isso é útil quando os usuários solicitam esses dados novamente durante a execução de um aplicativo. Quando os usuários solicitam dados, o mecanismo de banco de dados do Microsoft Access verifica esses dados no cache primeiro em vez de recuperá-los do servidor, o que leva mais tempo. O cache salva apenas dados provenientes de uma fonte de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="0cea2-p101">Data caching improves performance if you use **Recordset** objects to retrieve data from a remote server. A cache is a space in local memory that holds the data most recently retrieved from the server; this is useful if users request the data again while the application is running. When users request data, the Microsoft Access database engine checks the cache for the requested data first rather than retrieving it from the server, which takes more time. The cache only saves data that comes from an ODBC data source.</span></span>

<span data-ttu-id="0cea2-p102">Qualquer fonte de dados ODBC conectada ao mecanismo de banco de dados do Microsoft Access, como uma tabela vinculada, pode ter um cache local. Para criar o cache, abra um objeto **Recordset** a partir da fonte de dados remota, defina as propriedades **CacheSize** e **[CacheStart](recordset2-cachestart-property-dao.md)** e utilize o método **[FillCache](recordset2-fillcache-method-dao.md)** ou navegue pelos registros utilizando os métodos **Move**.</span><span class="sxs-lookup"><span data-stu-id="0cea2-p102">Any Microsoft Access database engine-connected ODBC data source, such as a linked table, can have a local cache. To create the cache, open a **Recordset** object from the remote data source, set the **CacheSize** and **[CacheStart](recordset2-cachestart-property-dao.md)** properties, and then use the **[FillCache](recordset2-fillcache-method-dao.md)** method, or step through the records by using the **Move** methods.</span></span>

<span data-ttu-id="0cea2-p103">A configuração da propriedade **CacheStart** é o indicador do primeiro registro no objeto **Recordset** a ser armazenado em cache. Você pode usar o indicador de qualquer registro para definir a propriedade **CacheStart**. Torne o registro que deve iniciar o cache o registro atual e defina a propriedade **CacheStart** igual à propriedade **[Bookmark](recordset2-bookmark-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="0cea2-p103">The **CacheStart** property setting is the bookmark of the first record in the **Recordset** object to be cached. You can use the bookmark of any record to set the **CacheStart** property. Make the record you want to start the cache the current record, and set the **CacheStart** property equal to the **[Bookmark](recordset2-bookmark-property-dao.md)** property.</span></span>

<span data-ttu-id="0cea2-118">O mecanismo de banco de dados do Microsoft Access solicita os registros dentro do intervalo de cache, a partir do cache, e solicita os registros fora do intervalo de cache a partir do servidor.</span><span class="sxs-lookup"><span data-stu-id="0cea2-118">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="0cea2-119">Os registros recuperados do cache não refletem as alterações feitas simultaneamente por outros usuários na fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="0cea2-119">Records retrieved from the cache don't reflect changes made concurrently to the source data by other users.</span></span>

<span data-ttu-id="0cea2-120">Para forçar uma atualização de todos os dados em cache, defina a propriedade **CacheSize** do objeto **Recordset** como 0, redefina-a para o tamanho do cache solicitado originalmente e use o método **FillCache**.</span><span class="sxs-lookup"><span data-stu-id="0cea2-120">To force an update of all the cached data, set the **CacheSize** property of the **Recordset** object to 0, re-set it to the size of the cache you originally requested, and then use the **FillCache** method.</span></span>

