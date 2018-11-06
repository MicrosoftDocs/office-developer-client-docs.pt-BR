---
title: Propriedade Parameter.Value (DAO)
TOCTitle: Value Property
ms:assetid: 7058f3cd-9102-c711-bc83-b1565a8b001c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195733(v=office.15)
ms:contentKeyID: 48545556
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 95086e811288bd70dce15a22319531b28a1ecd6c
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996724"
---
# <a name="parametervalue-property-dao"></a>Propriedade Parameter.Value (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Define ou retorna o valor de um objeto. **Variant** de leitura/gravação.

## <a name="syntax"></a>Sintaxe

*expressão* . Valor

*expressão* Uma variável que representa um objeto **Parameter** .

## <a name="remarks"></a>Comentários

O valor de definição ou de retorno é um tipo de dados Variant que avalia um valor adequado do tipo de dados, conforme especificado pela propriedade **Type** de um objeto.

Geralmente, a propriedade **Value** é usada para recuperar e alterar dados nos objetos **Recordset**.

A propriedade **Value** é a propriedade padrão dos objetos **Field**, **Parameter** e **Property**. Por esse motivo, defina ou retorne o valor de um desses objetos referindo-se diretamente a eles em vez de especificar a propriedade **Value**.

A tentativa de definição ou de retorno da propriedade **Value** em um contexto inadequado (por exemplo, a propriedade **Value** de um objeto **Field** na coleção **Fields** de um objeto **TableDef**) causará um erro interceptável.

> [!NOTE]
> Durante a leitura de valores decimais de um banco de dados do Microsoft SQL Server, esse valores serão formatados pela notação científica em um espaço de trabalho do Microsoft Access, mas aparecerão como valores decimais normais em um espaço de trabalho do ODBCDirect.


