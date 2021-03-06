---
title: Propriedade ParentRow (ADO)
TOCTitle: ParentRow property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2844f7c93164c4b384a895cd32a13bd682154ce3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287735"
---
# <a name="parentrow-property-ado"></a>Propriedade ParentRow (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Define o contêiner de um objeto **Row** do OLE DB em um objeto **ADORecordConstruction**, de forma que o pai da linha seja transformado em um objeto **Record** do ADO.

Somente gravação.

## <a name="syntax"></a>Sintaxe

HRESULT put \_ ParentRow( \[ in \] IUnknown \* pParent);

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*pParent* |O contêiner de uma linha.|

## <a name="return-values"></a>Valor de retorno

Esse método de propriedade retorna os valores HRESULT padrão, incluindo S \_ OK e E \_ FAIL.

## <a name="applies-to"></a>Aplicável a

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

