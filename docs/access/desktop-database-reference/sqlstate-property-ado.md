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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308545"
---
# <a name="sqlstate-property-ado"></a>Propriedade SQLState (ADO)


**Aplica-se ao:** Access 2013, Office 2013

Indica o estado do SQL de um determinado objeto [Error](error-object-ado.md).

## <a name="return-value"></a>Valor de retorno

Retorna um valor **String** de cinco caracteres que segue o padrão ANSI SQL e indica o código de erro.

## <a name="remarks"></a>Comentários

Utilize a propriedade **SQLState** para ler o código de erro de cinco caracteres que o provedor retornar quando ocorrer um erro durante o processamento de uma instrução SQL. Por exemplo, ao utillizar o Microsoft OLE DB Provider for ODBC com um banco de dados Microsoft SQL Server, os códigos de erro do estado do SQL serão originados do ODBC, com base nos erros específicos para o ODBC, ou em erros que se originaram do Microsoft SQL Server e, em seguida, serão mapeados para os erros do ODBC. Esses códigos de erro são documentados no padrão ANSI SQL, mas poderão ser implementados de formas diferentes por diversas fontes de dados.

