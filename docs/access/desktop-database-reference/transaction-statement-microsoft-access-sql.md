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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705516"
---
# <a name="transaction-statement-microsoft-access-sql"></a><span data-ttu-id="ae1ed-102">Instrução TRANSACTION (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="ae1ed-102">TRANSACTION statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="ae1ed-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="ae1ed-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ae1ed-104">Usada para iniciar e concluir transações explícitas.</span><span class="sxs-lookup"><span data-stu-id="ae1ed-104">Used to initiate and conclude explicit transactions.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae1ed-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ae1ed-105">Syntax</span></span>

<span data-ttu-id="ae1ed-106">**Iniciar uma nova transação**:</span><span class="sxs-lookup"><span data-stu-id="ae1ed-106">**Initiate a new transaction**:</span></span>

<span data-ttu-id="ae1ed-107">BEGIN TRANSACTION</span><span class="sxs-lookup"><span data-stu-id="ae1ed-107">BEGIN TRANSACTION</span></span>

<span data-ttu-id="ae1ed-108">**Conclude uma transação, confirmando que tudo funciona executado durante a transação**:</span><span class="sxs-lookup"><span data-stu-id="ae1ed-108">**Conclude a transaction by committing all work performed during the transaction**:</span></span>

<span data-ttu-id="ae1ed-109">Confirmar \[transação | TRABALHO\]</span><span class="sxs-lookup"><span data-stu-id="ae1ed-109">COMMIT \[TRANSACTION | WORK\]</span></span>

<span data-ttu-id="ae1ed-110">**Conclude uma transação, cancelando todo o trabalho executado durante a transação**:</span><span class="sxs-lookup"><span data-stu-id="ae1ed-110">**Conclude a transaction by rolling back all work performed during the transaction**:</span></span>

<span data-ttu-id="ae1ed-111">REVERSÃO \[transação | TRABALHO\]</span><span class="sxs-lookup"><span data-stu-id="ae1ed-111">ROLLBACK \[TRANSACTION | WORK\]</span></span>

## <a name="remarks"></a><span data-ttu-id="ae1ed-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="ae1ed-112">Remarks</span></span>

<span data-ttu-id="ae1ed-p101">As transações não são iniciadas automaticamente. Para iniciar uma transação, você deve ativá-la explicitamente, utilizando BEGIN TRANSACTION.</span><span class="sxs-lookup"><span data-stu-id="ae1ed-p101">Transactions are not started automatically. To start a transaction, you must do so explicitly using BEGIN TRANSACTION.</span></span>

<span data-ttu-id="ae1ed-p102">As transações podem ser aninhadas em até cinco níveis de profundidade. Para iniciar uma transação aninhada, use BEGIN TRANSACTION dentro do contexto de uma transação existente.</span><span class="sxs-lookup"><span data-stu-id="ae1ed-p102">Transactions can be nested up to five levels deep. To start a nested transaction, use BEGIN TRANSACTION within the context of an existing transaction.</span></span>

<span data-ttu-id="ae1ed-117">As transações não são aceitas em tabelas vinculadas.</span><span class="sxs-lookup"><span data-stu-id="ae1ed-117">Transactions are not supported for linked tables.</span></span>

