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
# <a name="transaction-statement-microsoft-access-sql"></a><span data-ttu-id="67110-102">Instrução TRANSACTION (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="67110-102">TRANSACTION statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="67110-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="67110-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="67110-104">Usada para iniciar e concluir transações explícitas.</span><span class="sxs-lookup"><span data-stu-id="67110-104">Used to initiate and conclude explicit transactions.</span></span>

## <a name="syntax"></a><span data-ttu-id="67110-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="67110-105">Syntax</span></span>

<span data-ttu-id="67110-106">**Iniciar uma nova transação**:</span><span class="sxs-lookup"><span data-stu-id="67110-106">**Initiate a new transaction**:</span></span>

<span data-ttu-id="67110-107">BEGIN TRANSACTION</span><span class="sxs-lookup"><span data-stu-id="67110-107">BEGIN TRANSACTION</span></span>

<span data-ttu-id="67110-108">**Conclude uma transação, confirmando que tudo funciona executado durante a transação**:</span><span class="sxs-lookup"><span data-stu-id="67110-108">**Conclude a transaction by committing all work performed during the transaction**:</span></span>

<span data-ttu-id="67110-109">Confirmar \[transação | TRABALHO\]</span><span class="sxs-lookup"><span data-stu-id="67110-109">COMMIT \[TRANSACTION | WORK\]</span></span>

<span data-ttu-id="67110-110">**Conclude uma transação, cancelando todo o trabalho executado durante a transação**:</span><span class="sxs-lookup"><span data-stu-id="67110-110">**Conclude a transaction by rolling back all work performed during the transaction**:</span></span>

<span data-ttu-id="67110-111">REVERSÃO \[transação | TRABALHO\]</span><span class="sxs-lookup"><span data-stu-id="67110-111">ROLLBACK \[TRANSACTION | WORK\]</span></span>

## <a name="remarks"></a><span data-ttu-id="67110-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="67110-112">Remarks</span></span>

<span data-ttu-id="67110-p101">As transações não são iniciadas automaticamente. Para iniciar uma transação, você deve ativá-la explicitamente, utilizando BEGIN TRANSACTION.</span><span class="sxs-lookup"><span data-stu-id="67110-p101">Transactions are not started automatically. To start a transaction, you must do so explicitly using BEGIN TRANSACTION.</span></span>

<span data-ttu-id="67110-p102">As transações podem ser aninhadas em até cinco níveis de profundidade. Para iniciar uma transação aninhada, use BEGIN TRANSACTION dentro do contexto de uma transação existente.</span><span class="sxs-lookup"><span data-stu-id="67110-p102">Transactions can be nested up to five levels deep. To start a nested transaction, use BEGIN TRANSACTION within the context of an existing transaction.</span></span>

<span data-ttu-id="67110-117">As transações não são aceitas em tabelas vinculadas.</span><span class="sxs-lookup"><span data-stu-id="67110-117">Transactions are not supported for linked tables.</span></span>

