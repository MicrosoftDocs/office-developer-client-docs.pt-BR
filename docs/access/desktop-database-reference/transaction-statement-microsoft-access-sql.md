---
title: Instrução TRANSACTION (Microsoft Access SQL)
TOCTitle: TRANSACTION Statement (Microsoft Access SQL)
ms:assetid: 481e807d-94e4-f201-adac-d25ee89d9220
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193241(v=office.15)
ms:contentKeyID: 48544614
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277472
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 13628ee6d384430691475eb06dbbbdce4e980103
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463756"
---
# <a name="transaction-statement-microsoft-access-sql"></a>Instrução TRANSACTION (Microsoft Access SQL)


**Aplica-se a**: Access 2013 | Office 2013

Usada para iniciar e concluir transações explícitas.

## <a name="syntax"></a>Sintaxe

Iniciar uma nova transação.

BEGIN TRANSACTION

Concluir uma transação, confirmando todo o trabalho executado durante a transação.

Confirmar \[transação | TRABALHO\]

Concluir uma transação, cancelando todo o trabalho executado durante a transação.

REVERSÃO \[transação | TRABALHO\]

## <a name="remarks"></a>Comentários

As transações não são iniciadas automaticamente. Para iniciar uma transação, você deve ativá-la explicitamente, utilizando BEGIN TRANSACTION.

As transações podem ser aninhadas em até cinco níveis de profundidade. Para iniciar uma transação aninhada, use BEGIN TRANSACTION dentro do contexto de uma transação existente.

As transações não são aceitas em tabelas vinculadas.

