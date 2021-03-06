---
title: Método Seek - ActiveX Data Objects (ADO)
TOCTitle: Seek method (ADO)
ms:assetid: cf0f133b-31f2-a2df-6cf3-1b5fa73b516c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250027(v=office.15)
ms:contentKeyID: 48547802
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 321040a39b02f31f0265df6e91748df13c05032c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308789"
---
# <a name="seek-method-ado"></a>Método Seek (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Pesquisa o índice de um [Recordset](recordset-object-ado.md) para localizar rapidamente a linha que corresponde aos valores especificados e altera a posição de linha atual para essa linha.

## <a name="syntax"></a>Sintaxe

*recordset*. Seek *KeyValues*, *SeekOption*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*KeyValues* |Uma matriz de valores **Variant**. Um índice consiste em uma ou mais colunas e a matriz contém um valor a ser comparado em relação a cada coluna correspondente.|
|*SeekOption* |Um valor [SeekEnum](seekenum.md) que especifica o tipo de comparação a ser feita entre as colunas do índice e os *KeyValues* correspondentes.|

## <a name="remarks"></a>Comentários

Use o método **Seek** junto com a propriedade [Index](index-property-ado.md) se o provedor subjacente oferecer suporte aos índices no objeto **Recordset**. Use o método [Supports](supports-method-ado.md)**(adSeek)** para determinar se o provedor subjacente oferece suporte ao método **Seek** e o método **Supports(adIndex)** para determinar se o provedor oferece suporte aos índices. (Por exemplo, o [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) oferece suporte a **Seek** e **Index**.)

Se **Seek** não localizar a linha desejada, nenhum erro ocorrerá e a linha será posicionada no final do **Recordset**. Defina a propriedade **Index** para o índice desejado antes de executar este método.

Este método é suportado apenas com cursores do servidor. Seek não é suportado quando o valor da propriedade **CursorLocation** do objeto [Recordset](cursorlocation-property-ado.md) for **adUseClient**.

Este método pode ser utilizado apenas quando o objeto **Recordset** foi aberto com um [CommandTypeEnum](commandtypeenum.md) com o valor **adCmdTableDirect**.

