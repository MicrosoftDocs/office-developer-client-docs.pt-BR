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
localization_priority: Priority
ms.openlocfilehash: 828bccfad83320d27f9473d532ab86f73b2fde98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314144"
---
# <a name="transaction-statement-microsoft-access-sql"></a>Instrução TRANSACTION (Microsoft Access SQL)

**Aplica-se ao**: Access 2013, Office 2013

Usado para iniciar e concluir transações explícitas.

## <a name="syntax"></a>Sintaxe

**Iniciar uma nova transação**:

INICIAR TRANSAÇÃO

**Conclui uma transação ao confirmar todo o trabalho executado durante a transação**:

CONFIRMAR \[TRANSAÇÃO | TRABALHO\]

**Conclui uma transação ao reverter todo o trabalho executado durante a transação**:

REVERSÃO \[TRANSAÇÃO | TRABALHO\]

## <a name="remarks"></a>Comentários

As transações não são iniciadas automaticamente. Para iniciar uma transação, faça isso explicitamente usando BEGIN TRANSACTION.

É possível aninhar transações até cinco níveis de profundidade. Para iniciar uma transação aninhada, use BEGIN TRANSACTION no contexto de uma transação existente.

Transações não são compatíveis com tabelas vinculadas.

