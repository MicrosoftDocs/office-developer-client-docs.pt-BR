---
title: Propriedade Campo2. Value (DAO)
TOCTitle: Value Property
ms:assetid: 6ead6ba8-1613-99c7-7968-56f5b81b2385
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195566(v=office.15)
ms:contentKeyID: 48545515
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4324917fcabd768a9527b11fceadbfc2dc9ef2b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292626"
---
# <a name="field2value-property-dao"></a>Propriedade Campo2. Value (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Define ou retorna o valor de um objeto. **Variant** de leitura/gravação.

## <a name="syntax"></a>Sintaxe

*expressão* . Valor

*expressão* Uma variável que representa um objeto **campo2** .

## <a name="remarks"></a>Comentários

O valor de definição ou de retorno é um tipo de dados Variant que avalia um valor adequado do tipo de dados, conforme especificado pela propriedade **Type** de um objeto.

Geralmente, a propriedade **Value** é usada para recuperar e alterar dados nos objetos **Recordset**.

A propriedade **Value** é a propriedade padrão dos objetos **Field2**, **Parameter** e **Property**. Por esse motivo, defina ou retorne o valor de um desses objetos referindo-se diretamente a eles em vez de especificar a propriedade **Value**.

A tentativa de definição ou de retorno da propriedade **Value** em um contexto inapropriado (por exemplo, a propriedade **Value** de um objeto **Field2** na coleção **Fields** de um objeto **TableDef**) causará um erro interceptável.


> [!NOTE]
> Durante a leitura de valores decimais de um banco de dados do Microsoft SQL Server, esse valores serão formatados pela notação científica em um espaço de trabalho do Microsoft Access, mas aparecerão como valores decimais normais em um espaço de trabalho do ODBCDirect.


