---
title: Propriedade NativeError (ADO)
TOCTitle: NativeError property (ADO)
ms:assetid: 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249731(v=office.15)
ms:contentKeyID: 48546685
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d572e7629deca0c7732bafbdfdb0c600ce34a35
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880177"
---
# <a name="nativeerror-property-ado"></a><span data-ttu-id="60c49-102">Propriedade NativeError (ADO)</span><span class="sxs-lookup"><span data-stu-id="60c49-102">NativeError property (ADO)</span></span>


<span data-ttu-id="60c49-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="60c49-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="60c49-104">Indica o código de erro específico do provedor para um determinado objeto [Error](error-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="60c49-104">Indicates the provider-specific error code for a given [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="60c49-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="60c49-105">Return value</span></span>

<span data-ttu-id="60c49-106">Retorna um valor **Long** que indica o código de erro.</span><span class="sxs-lookup"><span data-stu-id="60c49-106">Returns a **Long** value that indicates the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="60c49-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="60c49-107">Remarks</span></span>

<span data-ttu-id="60c49-p101">Use a propriedade **NativeError** para recuperar as informações de erro específicas do banco de dados para um determinado objeto **Error**. Por exemplo, ao usar o Microsoft ODBC Provider para OLE DB com um banco de dados Microsoft SQL Server, os códigos de erro nativos originados do SQL Server passam pelo ODBC e ODBC Provider para a propriedade **NativeError** do ADO.</span><span class="sxs-lookup"><span data-stu-id="60c49-p101">Use the **NativeError** property to retrieve the database-specific error information for a particular **Error** object. For example, when using the Microsoft ODBC Provider for OLE DB with a Microsoft SQL Server database, native error codes that originate from SQL Server pass through ODBC and the ODBC Provider to the ADO **NativeError** property.</span></span>

