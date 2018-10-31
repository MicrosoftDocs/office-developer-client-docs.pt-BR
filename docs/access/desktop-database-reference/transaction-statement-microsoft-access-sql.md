---
title: Instrução TRANSACTION (Microsoft Access SQL)
TOCTitle: TRANSACTION statement (Microsoft Access SQL)
ms:assetid: 481e807d-94e4-f201-adac-d25ee89d9220
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193241(v=office.15)
ms:contentKeyID: 48544614
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277472
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6d93fc90beded30d96b4db54c35ab3046da06899
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862653"
---
# <a name="transaction-statement-microsoft-access-sql"></a>Instrução TRANSACTION (Microsoft Access SQL)

**Aplica-se a**: Access 2013 | Office 2013

Usada para iniciar e concluir transações explícitas.

## <a name="syntax"></a>Sintaxe

**Iniciar uma nova transação**:

BEGIN TRANSACTION

**Conclude uma transação, confirmando que tudo funciona executado durante a transação**:

Confirmar \[transação | TRABALHO\]

**Conclude uma transação, cancelando todo o trabalho executado durante a transação**:

REVERSÃO \[transação | TRABALHO\]

## <a name="remarks"></a>Comentários

As transações não são iniciadas automaticamente. Para iniciar uma transação, você deve ativá-la explicitamente, utilizando BEGIN TRANSACTION.

As transações podem ser aninhadas em até cinco níveis de profundidade. Para iniciar uma transação aninhada, use BEGIN TRANSACTION dentro do contexto de uma transação existente.

As transações não são aceitas em tabelas vinculadas.

