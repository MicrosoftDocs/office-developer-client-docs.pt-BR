---
title: Propriedade Chapter (ADO)
TOCTitle: Chapter property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d7523a930feed7431bf8be0bbb7222a4b305483
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949394"
---
# <a name="chapter-property-ado"></a>Propriedade Chapter (ADO)

**Aplica-se a**: Access 2013, o Office 2013
 
Obtém ou configura um objeto **Chapter** do OLE DB de/em um objeto **ADORecordsetConstruction**. Quando você usa **colocar\_capítulo** para definir o objeto de **capítulo** , um subconjunto de linhas seja transformado em um objeto **Recordset** do ADO. Isso define o capítulo atual do objeto **Rowset**. Leitura/gravação.

## <a name="syntax"></a>Sintaxe

Get HRESULT\_capítulo (\[check-out, retval\] longo\* plChapter);

Colocar HRESULT\_capítulo (\[na\] lChapter longo);

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*plChapter* |Ponteiro para o identificador de um capítulo.|
|*LChapter* |Identificador de um capítulo.|

## <a name="return-values"></a>Valor de retorno

Esse método de propriedade retorna os valores padrão HRESULT, incluindo S\_Okey e f\_falhar.

## <a name="applies-to"></a>Aplica-se a

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

