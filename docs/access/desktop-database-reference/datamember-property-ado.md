---
title: Propriedade DataMember (ADO)
TOCTitle: DataMember property (ADO)
ms:assetid: f89e1d42-7993-764b-4e8a-2f449903f792
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250263(v=office.15)
ms:contentKeyID: 48548787
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eebd4e485c358ed141e6bcb5dc84c82d41fd88ed
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870146"
---
# <a name="datamember-property-ado"></a>Propriedade DataMember (ADO)

**Aplica-se a**: Access 2013, o Office 2013

Indica o nome do membro de dados que será recuperado do objeto referido pela propriedade [DataSource](datasource-property-ado.md).

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **String**. O nome não diferencia maiúsculas e minúsculas.

## <a name="remarks"></a>Comentários

Essa propriedade é usada para criar controles vinculados a dados no Ambiente de Dados. O Ambiente de Dados mantém as coleções de dados (fontes de dados) contendo objetos nomeados (*membros de dados*) que serão representados como um objeto [Recordset](recordset-object-ado.md)*.*

As propriedades **DataMember** e **DataSource** devem ser usadas em conjunto.

A propriedade **DataMember** determina qual objeto especificado pela propriedade **DataSource** será representado como um objeto **Recordset**. O objeto **Recordset** deve ser fechado antes que essa propriedade seja definida. Ocorrerá um erro se a propriedade **DataMember** não for definida antes da propriedade **DataSource** ou se o nome do **DataMember** não for reconhecido pelo objeto especificado na propriedade **DataSource**.

**Uso**

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
