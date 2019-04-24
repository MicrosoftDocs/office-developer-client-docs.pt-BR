---
title: Propriedade Chapter (ADO)
TOCTitle: Chapter property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b4f4efc2ffab9f7996b2d805658b985badbaf87e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296392"
---
# <a name="chapter-property-ado"></a>Propriedade Chapter (ADO)

**Aplica-se ao:** Access 2013, Office 2013
 
Obtém ou configura um objeto **Chapter** do OLE DB de/em um objeto **ADORecordsetConstruction**. Quando você usa **o\_Chapter** para definir o objeto **Chapter** , um subconjunto de linhas é transformado em um objeto **Recordset** do ADO. Isso define o capítulo atual do objeto **Rowset**. Leitura/gravação.

## <a name="syntax"></a>Sintaxe

HRESULT obter\_capítulo (\[out, retval\] Long\* plChapter);

Módulo HRESULT\_put (\[em\] Long lChapter);

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*plChapter* |Ponteiro para o identificador de um capítulo.|
|*LChapter* |Identificador de um capítulo.|

## <a name="return-values"></a>Valor de retorno

Este método de propriedade retorna os valores HRESULT padrão, incluindo\_S OK E\_o e falha.

## <a name="applies-to"></a>Aplica-se a

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

