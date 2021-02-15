---
title: Método Supports (ADO)
TOCTitle: Supports method (ADO)
ms:assetid: 2b4062ce-44df-4e84-1ce9-d6618c10c2af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249059(v=office.15)
ms:contentKeyID: 48543924
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 42447614c5fc58bc4eb2933354908693adf68ce6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308460"
---
# <a name="supports-method-ado"></a>Método Supports (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Determina se um objeto [Recordset](recordset-object-ado.md) especificado suporta um tipo de funcionalidade específico.

## <a name="syntax"></a>Sintaxe

*booliana*  =  *recordset*. Supports (*CursorOptions*)

## <a name="return-value"></a>Valor de retorno

Retorna um valor **Boolean** que indica se todos os recursos identificados pelo argumento *CursorOptions* são suportados pelo provedor.

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*CursorOptions* |Uma expressão **Long** que consiste em um ou mais valores [CursorOptionEnum](cursoroptionenum.md).|

## <a name="remarks"></a>Comentários

Utilize o método **Supports** para determinar quais tipos de funcionalidade um objeto **Recordset** suporta. Se o objeto **Recordset** suportar os recursos cujas constantes correspondentes estão em *CursorOptions*, o método **Supports** retornará **True**. Caso contrário, ele retornará **False**.


> [!NOTE]
> [!OBSERVAçãO] Embora o método **Supports** possa retornar **True** para uma determinada funcionalidade, isso não garante que o provedor possa tornar o recurso disponível sob todas as circunstâncias. O método **Supports** simplesmente retorna se o provedor pode suportar a funcionalidade especificada, supondo que determinadas condições sejam atendidas. Por exemplo, o método **Supports** pode indicar que um objeto **Recordset** suporta atualizações, muito embora o cursor tenha como base uma junção de várias tabelas, algumas colunas das quais não são atualizáveis.


