---
title: Propriedade ParentRow (ADO)
TOCTitle: ParentRow property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 28f0d1c7dbc0e062ff133b9f9997f1a737c3262e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872127"
---
# <a name="parentrow-property-ado"></a>Propriedade ParentRow (ADO)


**Aplica-se a**: Access 2013, o Office 2013


Define o contêiner de um objeto **Row** do OLE DB em um objeto **ADORecordConstruction**, de forma que o pai da linha seja transformado em um objeto **Record** do ADO.

Somente gravação.

## <a name="syntax"></a>Sintaxe

Colocar HRESULT\_ParentRow (\[na\] IUnknown\* pParent);

## <a name="parameters"></a>Parâmetros

  - *pParent*

  - O contêiner de uma linha.

## <a name="return-values"></a>Valor de retorno

Esse método de propriedade retorna os valores padrão HRESULT, incluindo S\_Okey e f\_falhar.

## <a name="applies-to"></a>Aplica-se a

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

