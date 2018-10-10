---
title: Propriedade ParentRow (ADO)
TOCTitle: ParentRow Property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 834dcaed7d1acdcf66410584436e2ccee8c91c56
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465443"
---
# <a name="parentrow-property-ado"></a>Propriedade ParentRow (ADO)


**Aplica-se a**: Access 2013 | Office 2013


Define o contêiner de um objeto **Row** do OLE DB em um objeto **ADORecordConstruction**, de forma que o pai da linha seja transformado em um objeto **Record** do ADO.

Somente gravação.

## <a name="syntax"></a>Sintaxe

Colocar HRESULT\_ParentRow (\[na\] IUnknown\* pParent);

## <a name="parameters"></a>Parâmetros

  - *pParent*

  - O contêiner de uma linha.

## <a name="return-values"></a>Valores de retorno

Esse método de propriedade retorna os valores padrão HRESULT, incluindo S\_Okey e f\_falhar.

## <a name="applies-to"></a>Aplica-se a

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

