---
title: Propriedade NativeError (ADO)
TOCTitle: NativeError property (ADO)
ms:assetid: 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249731(v=office.15)
ms:contentKeyID: 48546685
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 86734d77cafd8dbe3c26219e291c16b81ef0026b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288607"
---
# <a name="nativeerror-property-ado"></a><span data-ttu-id="51a5a-102">Propriedade NativeError (ADO)</span><span class="sxs-lookup"><span data-stu-id="51a5a-102">NativeError property (ADO)</span></span>


<span data-ttu-id="51a5a-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="51a5a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="51a5a-104">Indica o código de erro específico do provedor para um determinado objeto [Error](error-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="51a5a-104">Indicates the provider-specific error code for a given [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="51a5a-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="51a5a-105">Return value</span></span>

<span data-ttu-id="51a5a-106">Retorna um valor **Long** que indica o código de erro.</span><span class="sxs-lookup"><span data-stu-id="51a5a-106">Returns a **Long** value that indicates the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="51a5a-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="51a5a-107">Remarks</span></span>

<span data-ttu-id="51a5a-p101">Use a propriedade **NativeError** para recuperar as informações de erro específicas do banco de dados para um determinado objeto **Error**. Por exemplo, ao usar o Microsoft ODBC Provider para OLE DB com um banco de dados Microsoft SQL Server, os códigos de erro nativos originados do SQL Server passam pelo ODBC e ODBC Provider para a propriedade **NativeError** do ADO.</span><span class="sxs-lookup"><span data-stu-id="51a5a-p101">Use the **NativeError** property to retrieve the database-specific error information for a particular **Error** object. For example, when using the Microsoft ODBC Provider for OLE DB with a Microsoft SQL Server database, native error codes that originate from SQL Server pass through ODBC and the ODBC Provider to the ADO **NativeError** property.</span></span>

