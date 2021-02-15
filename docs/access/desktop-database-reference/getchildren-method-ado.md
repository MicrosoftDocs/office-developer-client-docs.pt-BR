---
title: Método GetChildren (ADO)
TOCTitle: GetChildren method (ADO)
ms:assetid: 998cf640-ffc7-51e1-4d1e-4797f7cdea4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249687(v=office.15)
ms:contentKeyID: 48546515
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4ca8c113a377543ea8624972adb5958612a3fc72
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292304"
---
# <a name="getchildren-method-ado"></a>Método GetChildren (ADO)


**Aplica-se ao:** Access 2013, Office 2013


Retorna um [Recordset](recordset-object-ado.md) cujas linhas representam os filhos de uma coleção [Record](record-object-ado.md).

## <a name="syntax"></a>Sintaxe

**Definir** *registro do conjunto de*  =  *registros.* GetChildren

## <a name="return-value"></a>Valor de retorno

Um objeto **Recordset** para o qual cada linha representa um filho do objeto **Record** atual. Por exemplo, os filhos de um **Record** que representa um diretório seriam os arquivos e subdiretórios contidos no diretório pai.

## <a name="remarks"></a>Comentários

O provedor determina quais colunas existem no **Recordset** retornado. Por exemplo, um provedor de fonte de documento sempre retorna um **Recordset** de recursos.

