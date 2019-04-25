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
# <a name="transaction-statement-microsoft-access-sql"></a><span data-ttu-id="04c32-102">Instrução TRANSACTION (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="04c32-102">TRANSACTION Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="04c32-103">**Aplica-se ao**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="04c32-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="04c32-104">Usado para iniciar e concluir transações explícitas.</span><span class="sxs-lookup"><span data-stu-id="04c32-104">Used to initiate and conclude explicit transactions.</span></span>

## <a name="syntax"></a><span data-ttu-id="04c32-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="04c32-105">Syntax</span></span>

<span data-ttu-id="04c32-106">**Iniciar uma nova transação**:</span><span class="sxs-lookup"><span data-stu-id="04c32-106">Initiate a new transaction.</span></span>

<span data-ttu-id="04c32-107">INICIAR TRANSAÇÃO</span><span class="sxs-lookup"><span data-stu-id="04c32-107">BEGIN TRANSACTION</span></span>

<span data-ttu-id="04c32-108">**Conclui uma transação ao confirmar todo o trabalho executado durante a transação**:</span><span class="sxs-lookup"><span data-stu-id="04c32-108">Conclude a transaction by committing all work performed during the transaction.</span></span>

<span data-ttu-id="04c32-109">CONFIRMAR \[TRANSAÇÃO | TRABALHO\]</span><span class="sxs-lookup"><span data-stu-id="04c32-109">COMMIT [TRANSACTION | WORK]</span></span>

<span data-ttu-id="04c32-110">**Conclui uma transação ao reverter todo o trabalho executado durante a transação**:</span><span class="sxs-lookup"><span data-stu-id="04c32-110">Conclude a transaction by rolling back all work performed during the transaction.</span></span>

<span data-ttu-id="04c32-111">REVERSÃO \[TRANSAÇÃO | TRABALHO\]</span><span class="sxs-lookup"><span data-stu-id="04c32-111">ROLLBACK [TRANSACTION | WORK]</span></span>

## <a name="remarks"></a><span data-ttu-id="04c32-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="04c32-112">Remarks</span></span>

<span data-ttu-id="04c32-p101">As transações não são iniciadas automaticamente. Para iniciar uma transação, faça isso explicitamente usando BEGIN TRANSACTION.</span><span class="sxs-lookup"><span data-stu-id="04c32-p101">Transactions are not started automatically. To start a transaction, you must do so explicitly using BEGIN TRANSACTION.</span></span>

<span data-ttu-id="04c32-p102">É possível aninhar transações até cinco níveis de profundidade. Para iniciar uma transação aninhada, use BEGIN TRANSACTION no contexto de uma transação existente.</span><span class="sxs-lookup"><span data-stu-id="04c32-p102">Transactions can be nested up to five levels deep. To start a nested transaction, use BEGIN TRANSACTION within the context of an existing transaction.</span></span>

<span data-ttu-id="04c32-117">Transações não são compatíveis com tabelas vinculadas.</span><span class="sxs-lookup"><span data-stu-id="04c32-117">Transactions are not supported for linked tables.</span></span>

