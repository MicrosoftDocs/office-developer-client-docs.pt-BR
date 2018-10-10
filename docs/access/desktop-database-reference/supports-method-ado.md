---
title: Método Supports (ADO)
TOCTitle: Supports Method (ADO)
ms:assetid: 2b4062ce-44df-4e84-1ce9-d6618c10c2af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249059(v=office.15)
ms:contentKeyID: 48543924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 61e6a4f3a5771c4d223380160204e4b0b350f210
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25461987"
---
# <a name="supports-method-ado"></a>Método Supports (ADO)


**Aplica-se a**: Access 2013 | Office 2013

Determina se um objeto [Recordset](recordset-object-ado.md) especificado suporta um tipo de funcionalidade específico.

## <a name="syntax"></a>Sintaxe

*Boolean* = *recordset*. Suporta (*CursorOptions*)

## <a name="return-value"></a>Valor retornado

Retorna um valor **Boolean** que indica se todos os recursos identificados pelo argumento *CursorOptions* são suportados pelo provedor.

## <a name="parameters"></a>Parâmetros

  - *CursorOptions*

  - Uma expressão **Long** que consiste em um ou mais valores [CursorOptionEnum](cursoroptionenum.md).

## <a name="remarks"></a>Comentários

Utilize o método **Supports** para determinar quais tipos de funcionalidade um objeto **Recordset** suporta. Se o objeto **Recordset** suportar os recursos cujas constantes correspondentes estão em *CursorOptions*, o método **Supports** retornará **True**. Caso contrário, ele retornará **False**.


> [!NOTE]
> <P>[!OBSERVAçãO] Embora o método <STRONG>Supports</STRONG> possa retornar <STRONG>True</STRONG> para uma determinada funcionalidade, isso não garante que o provedor possa tornar o recurso disponível sob todas as circunstâncias. O método <STRONG>Supports</STRONG> simplesmente retorna se o provedor pode suportar a funcionalidade especificada, supondo que determinadas condições sejam atendidas. Por exemplo, o método <STRONG>Supports</STRONG> pode indicar que um objeto <STRONG>Recordset</STRONG> suporta atualizações, muito embora o cursor tenha como base uma junção de várias tabelas, algumas colunas das quais não são atualizáveis.</P>


