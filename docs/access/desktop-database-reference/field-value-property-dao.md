---
title: Propriedade Field.Value (DAO)
TOCTitle: Value Property
ms:assetid: 6c0f9a8d-f51a-b8cf-8830-f8d960a1d08c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195493(v=office.15)
ms:contentKeyID: 48545465
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 946ce8ec4219229e047d1bef5c3ff6de403eb7c9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462772"
---
# <a name="fieldvalue-property-dao"></a>Propriedade Field.Value (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Define ou retorna o valor de um objeto. **Variant** de leitura/gravação.

## <a name="syntax"></a>Sintaxe

*expressão* . Valor

*expressão* Uma variável que representa um objeto **Field** .

## <a name="remarks"></a>Comentários

O valor de definição ou de retorno é um tipo de dados Variant que avalia um valor adequado do tipo de dados, conforme especificado pela propriedade **Type** de um objeto.

Geralmente, a propriedade **Value** é usada para recuperar e alterar dados nos objetos **Recordset**.

A propriedade **Value** é a propriedade padrão dos objetos **Field**, **Parameter** e **Property**. Por esse motivo, defina ou retorne o valor de um desses objetos referindo-se diretamente a eles em vez de especificar a propriedade **Value**.

A tentativa de definição ou de retorno da propriedade **Value** em um contexto inadequado (por exemplo, a propriedade **Value** de um objeto **Field** na coleção **Fields** de um objeto **TableDef**) causará um erro interceptável.


> [!NOTE]
> <P>Durante a leitura de valores decimais de um banco de dados do Microsoft SQL Server, esse valores serão formatados pela notação científica em um espaço de trabalho do Microsoft Access, mas aparecerão como valores decimais normais em um espaço de trabalho do ODBCDirect.</P>


