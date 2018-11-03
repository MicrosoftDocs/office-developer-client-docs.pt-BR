---
title: Método - ActiveX Data Objects (ADO) Seek
TOCTitle: Seek method (ADO)
ms:assetid: cf0f133b-31f2-a2df-6cf3-1b5fa73b516c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250027(v=office.15)
ms:contentKeyID: 48547802
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: be8127ea3f298a8f137012615b1f4de656a6ea1f
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949709"
---
# <a name="seek-method-ado"></a>Método Seek (ADO)

**Aplica-se a**: Access 2013, o Office 2013

Pesquisa o índice de um [Recordset](recordset-object-ado.md) para localizar rapidamente a linha que corresponde aos valores especificados e altera a posição de linha atual para essa linha.

## <a name="syntax"></a>Sintaxe

*conjunto de registros*. Seek*KeyValues*, *SeekOption*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*KeyValues* |Uma matriz de valores **Variant**. Um índice consiste em uma ou mais colunas e a matriz contém um valor a ser comparado em relação a cada coluna correspondente.|
|*SeekOption* |Um valor [SeekEnum](seekenum.md) que especifica o tipo de comparação a ser feita entre as colunas do índice e os *KeyValues* correspondentes.|

## <a name="remarks"></a>Comentários

Use o método **Seek** junto com a propriedade [Index](index-property-ado.md) se o provedor subjacente oferecer suporte aos índices no objeto **Recordset**. Use o método **(adSeek)** [oferece suporte](supports-method-ado.md)para determinar se o provedor subjacente suporta **Seek**e o método **Supports(adIndex)** para determinar se o provedor oferece suporte a índices. (Por exemplo, o [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) oferece suporte a **Seek** e **Index**.)

Se **Seek** não localizar a linha desejada, nenhum erro ocorrerá e a linha será posicionada no final do **Recordset**. Defina a propriedade **Index** para o índice desejado antes de executar este método.

Este método é suportado apenas com cursores do servidor. Seek não é suportado quando o valor da propriedade **CursorLocation** do objeto [Recordset](cursorlocation-property-ado.md) for **adUseClient**.

Este método pode ser utilizado apenas quando o objeto **Recordset** foi aberto com um [CommandTypeEnum](commandtypeenum.md) com o valor **adCmdTableDirect**.

