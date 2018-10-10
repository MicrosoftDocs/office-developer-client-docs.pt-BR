---
title: Propriedade NativeError (ADO)
TOCTitle: NativeError Property (ADO)
ms:assetid: 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249731(v=office.15)
ms:contentKeyID: 48546685
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b98d9695e29df63371b5ee375f864e7b1d4961ba
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465354"
---
# <a name="nativeerror-property-ado"></a>Propriedade NativeError (ADO)


**Aplica-se a**: Access 2013 | Office 2013

Indica o código de erro específico do provedor para um determinado objeto [Error](error-object-ado.md).

## <a name="return-value"></a>Valor de retorno

Retorna um valor **Long** que indica o código de erro.

## <a name="remarks"></a>Comentários

Use a propriedade **NativeError** para recuperar as informações de erro específicas do banco de dados para um determinado objeto **Error**. Por exemplo, ao usar o Microsoft ODBC Provider para OLE DB com um banco de dados Microsoft SQL Server, os códigos de erro nativos originados do SQL Server passam pelo ODBC e ODBC Provider para a propriedade **NativeError** do ADO.

