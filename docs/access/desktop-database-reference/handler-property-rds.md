---
title: Propriedade Handler (RDS)
TOCTitle: Handler Property (RDS)
ms:assetid: aaf8c8c6-f95b-3cf3-b3f6-203f37464c87
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249792(v=office.15)
ms:contentKeyID: 48546962
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2a020dfa5935cfe6a0b942c5234eda2a91c40d51
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463583"
---
# <a name="handler-property-rds"></a>Propriedade Handler (RDS)


**Aplica-se a**: Access 2013 | Office 2013


Indica o nome de um programa de personalização do servidor (manipulador) que estende a funcionalidade do [RDSServer.DataFactory](datafactory-object-rdsserver.md) e qualquer parâmetro usado pelo *manipulador*.

## <a name="syntax"></a>Sintaxe

*DataControl*. Manipulador = *cadeia de caracteres*

## <a name="parameters"></a>Parâmetros

  - *DataControl*

  - Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).

  - *String*

  - Um valor **String** que contém o nome do manipulador e qualquer parâmetro, todos separado por vírgulas (por exemplo, "handlerName, parm1, parm2,..., parm *N"*).

## <a name="remarks"></a>Comentários

Esta propriedade oferece suporte à personalização, uma funcionalidade que requer a definição da propriedade [CursorLocation](cursorlocation-property-ado.md) como **adUseClient**.

O nome do manipulador e seus parâmetros, se houver, são separados por vírgulas (","). Um comportamento imprevisível ocorrerá se um ponto-e-vírgula (";") aparecer em qualquer lugar dentro do *String*. Você pode compor seu próprio manipulador, desde que ele ofereça suporte à interface **IDataFactoryHandler**.

O nome do manipulador padrão é **MSDFMAP.Handler** e seu parâmetro padrão é um arquivo de personalização chamado **MSDFMAP.INI**. Use esta propriedade para invocar arquivos de personalização alternativos pelo administrador do servidor.

A alternativa para definir a propriedade **Handler** é especificar um manipulador e os parâmetros na propriedade [ConnectionString](connectionstring-property-ado.md) ; ou seja, "**manipulador = * * * handlerName, parm1, parm2,...;*".
