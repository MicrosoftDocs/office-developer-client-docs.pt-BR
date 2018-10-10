---
title: Método GetChildren (ADO)
TOCTitle: GetChildren Method (ADO)
ms:assetid: 998cf640-ffc7-51e1-4d1e-4797f7cdea4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249687(v=office.15)
ms:contentKeyID: 48546515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a11f3e34f8dcb45bab88d8ff87e69067103e4640
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462488"
---
# <a name="getchildren-method-ado"></a>Método GetChildren (ADO)


**Aplica-se a**: Access 2013 | Office 2013


Retorna um [Recordset](recordset-object-ado.md) cujas linhas representam os filhos de uma coleção [Record](record-object-ado.md).

## <a name="syntax"></a>Sintaxe

**Definir** *conjunto de registros*  =  *registro*. GetChildren

## <a name="return-value"></a>Valor de Retorno

Um objeto **Recordset** para o qual cada linha representa um filho do objeto **Record** atual. Por exemplo, os filhos de um **Record** que representa um diretório seriam os arquivos e subdiretórios contidos no diretório pai.

## <a name="remarks"></a>Comentários

O provedor determina quais colunas existem no **Recordset** retornado. Por exemplo, um provedor de fonte de documento sempre retorna um **Recordset** de recursos.
