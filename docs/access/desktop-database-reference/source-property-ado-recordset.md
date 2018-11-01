---
title: Propriedade Source (Recordset do ADO)
TOCTitle: Source Property (ADO Recordset)
ms:assetid: 523ea81e-d011-8d87-436e-084b6eba0908
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249269(v=office.15)
ms:contentKeyID: 48544843
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 32d3d44094e9e5922b7c5e0cfa59ccd1f344ef0f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879134"
---
# <a name="source-property-ado-recordset"></a>Propriedade Source (Recordset do ADO)


**Aplica-se a**: Access 2013, o Office 2013

Indica a fonte de dados de um objeto [Recordset](recordset-object-ado.md).

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define um valor **String** ou a referência de objeto [Command](command-object-ado.md); retorna somente um valor **String** que indica a origem do **Recordset**.

## <a name="remarks"></a>Comentários

Utilize a propriedade **Source** para especificar uma fonte de dados para um objeto **Recordset** utilizando uma das seguintes opções: uma variável de objeto **Command**, uma instrução SQL, um procedimento armazenado ou um nome de tabela.

Se você definir a propriedade **Source** para um objeto **Command**, a propriedade [ActiveConnection](activeconnection-property-ado.md) do objeto **Recordset** herdará o valor da propriedade **ActiveConnection** para o objeto **Command** especificado. Entretanto, a leitura da propriedade **Source** não retornará o objeto **Command**; em vez disso, retornará a propriedade [CommandText](commandtext-property-ado.md) do objeto **Command** para o qual você definiu a propriedade **Source**.

Se a propriedade **Source** é uma instrução SQL, um procedimento armazenado ou um nome de tabela, você pode otimizar o desempenho, passando o argumento adequado *Options* com a chamada do método [Open](open-method-ado-recordset.md) .

A propriedade **Source** é leitura/gravação para objetos **Recordset** fechados e somente leitura para objetos **Recordset** abertos.

