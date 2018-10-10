---
title: Propriedade Rowset (ADO)
TOCTitle: Rowset Property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 95a33fb3d24e5cdbf608d268781be0dd536fa315
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463676"
---
# <a name="rowset-property-ado"></a>Propriedade Rowset (ADO)


**Aplica-se a**: Access 2013 | Office 2013



Obtém ou define um objeto **Rowset** do OLE DB a partir de/em um objeto **ADORecordsetConstruction**. Quando você usa put\_Rowset, o conjunto de linhas seja transformado em um objeto **Recordset** do ADO.

Leitura/gravação.

## <a name="syntax"></a>Sintaxe

Get HRESULT\_Rowset (\[check-out, retval\] IUnknown\* \* ppRowset);

Colocar HRESULT\_Rowset (\[na\] IUnknown\* pRowset);

## <a name="parameters"></a>Parâmetros

  - *ppRowset*

  - Ponteiro para um objeto **Rowset** do OLE DB.

  - *PRowset*

  - Um objeto **Rowset** do OLE DB.

## <a name="return-values"></a>Valores de retorno

Esse método de propriedade retorna os valores padrão HRESULT, incluindo S\_Okey e f\_falhar.

## <a name="applies-to"></a>Aplica-se a

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)
