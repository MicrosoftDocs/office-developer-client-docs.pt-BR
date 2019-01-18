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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705943"
---
# <a name="nativeerror-property-ado"></a>Propriedade NativeError (ADO)


**Aplica-se a**: Access 2013, o Office 2013

Indica o código de erro específico do provedor para um determinado objeto [Error](error-object-ado.md).

## <a name="return-value"></a>Valor de retorno

Retorna um valor **Long** que indica o código de erro.

## <a name="remarks"></a>Comentários

Use a propriedade **NativeError** para recuperar as informações de erro específicas do banco de dados para um determinado objeto **Error**. Por exemplo, ao usar o Microsoft ODBC Provider para OLE DB com um banco de dados Microsoft SQL Server, os códigos de erro nativos originados do SQL Server passam pelo ODBC e ODBC Provider para a propriedade **NativeError** do ADO.

