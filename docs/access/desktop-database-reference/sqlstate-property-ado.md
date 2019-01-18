---
title: Propriedade SQLState (ADO)
TOCTitle: SQLState property (ADO)
ms:assetid: cf3b078a-849e-1ad2-cba4-a26160080868
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250029(v=office.15)
ms:contentKeyID: 48547806
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: eb4a9adbc6060b7c33e128a0a3fca8c1eb7bc10d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716296"
---
# <a name="sqlstate-property-ado"></a><span data-ttu-id="1532f-102">Propriedade SQLState (ADO)</span><span class="sxs-lookup"><span data-stu-id="1532f-102">SQLState property (ADO)</span></span>


<span data-ttu-id="1532f-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="1532f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1532f-104">Indica o estado do SQL de um determinado objeto [Error](error-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="1532f-104">Indicates the SQL state for a given [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="1532f-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1532f-105">Return value</span></span>

<span data-ttu-id="1532f-106">Retorna um valor **String** de cinco caracteres que segue o padrão ANSI SQL e indica o código de erro.</span><span class="sxs-lookup"><span data-stu-id="1532f-106">Returns a five-character **String** value that follows the ANSI SQL standard and indicates the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1532f-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="1532f-107">Remarks</span></span>

<span data-ttu-id="1532f-p101">Utilize a propriedade **SQLState** para ler o código de erro de cinco caracteres que o provedor retornar quando ocorrer um erro durante o processamento de uma instrução SQL. Por exemplo, ao utillizar o Microsoft OLE DB Provider for ODBC com um banco de dados Microsoft SQL Server, os códigos de erro do estado do SQL serão originados do ODBC, com base nos erros específicos para o ODBC, ou em erros que se originaram do Microsoft SQL Server e, em seguida, serão mapeados para os erros do ODBC. Esses códigos de erro são documentados no padrão ANSI SQL, mas poderão ser implementados de formas diferentes por diversas fontes de dados.</span><span class="sxs-lookup"><span data-stu-id="1532f-p101">Use the **SQLState** property to read the five-character error code that the provider returns when an error occurs during the processing of an SQL statement. For example, when using the Microsoft OLE DB Provider for ODBC with a Microsoft SQL Server database, SQL state error codes originate from ODBC, based either on errors specific to ODBC or on errors that originate from Microsoft SQL Server, and are then mapped to ODBC errors. These error codes are documented in the ANSI SQL standard, but may be implemented differently by different data sources.</span></span>

