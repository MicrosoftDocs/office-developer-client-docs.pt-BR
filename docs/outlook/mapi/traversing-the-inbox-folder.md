---
title: Desviar a pasta da caixa de entrada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ad1459f-d59a-4784-94ea-4cad194e6e50
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 87fcde5a28a30f08bc2fd5f28fb692a4b4251fbf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770631"
---
# <a name="traversing-the-inbox-folder"></a><span data-ttu-id="33756-103">Desviar a pasta da caixa de entrada</span><span class="sxs-lookup"><span data-stu-id="33756-103">Traversing the Inbox Folder</span></span>

  
  
<span data-ttu-id="33756-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="33756-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="33756-105">**Para percorrer todas as mensagens na caixa de entrada**</span><span class="sxs-lookup"><span data-stu-id="33756-105">**To cycle through all of the messages in the Inbox**</span></span>
  
1. <span data-ttu-id="33756-106">Chame [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) para recuperar o identificador de entrada da caixa de entrada.</span><span class="sxs-lookup"><span data-stu-id="33756-106">Call [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to retrieve the entry identifier of the Inbox.</span></span> 
    
2. <span data-ttu-id="33756-107">Chame **IMAPIFolder::OpenEntry** para abrir a caixa de entrada.</span><span class="sxs-lookup"><span data-stu-id="33756-107">Call **IMAPIFolder::OpenEntry** to open the Inbox.</span></span> 
    
3. <span data-ttu-id="33756-108">Chame o método de [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) da caixa de entrada para recuperar a tabela de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="33756-108">Call the Inbox's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to retrieve the contents table.</span></span> 
    
4. <span data-ttu-id="33756-109">Chame o conteúdo método de [IMAPITable::SetColumns](imapitable-setcolumns.md) da tabela para limitar a coluna definida como **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) e quaisquer outras colunas que você precisar.</span><span class="sxs-lookup"><span data-stu-id="33756-109">Call the contents table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to limit the column set to **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) and any other columns you require.</span></span> 
    
5. <span data-ttu-id="33756-110">Chame [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar um grupo de linhas.</span><span class="sxs-lookup"><span data-stu-id="33756-110">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve a group of rows.</span></span> 
    
6. <span data-ttu-id="33756-111">Até que não existem mais quaisquer linhas na tabela de conteúdo:</span><span class="sxs-lookup"><span data-stu-id="33756-111">Until there are no longer any rows in the contents table:</span></span>
    
1. <span data-ttu-id="33756-112">Chame [IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir a mensagem representada pelo identificador de entrada de cada linha.</span><span class="sxs-lookup"><span data-stu-id="33756-112">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the message represented by the entry identifier from each row.</span></span> 
    
2. <span data-ttu-id="33756-113">Atribua o parâmetro _lppUnk_ para um ponteiro de interface **IMessage** local.</span><span class="sxs-lookup"><span data-stu-id="33756-113">Assign the  _lppUnk_ parameter to a local **IMessage** interface pointer.</span></span> 
    
3. <span data-ttu-id="33756-114">Trabalhar com as propriedades da mensagem.</span><span class="sxs-lookup"><span data-stu-id="33756-114">Work with the properties of the message.</span></span>
    
4. <span data-ttu-id="33756-115">Libere o ponteiro apontado pelo parâmetro _lppUnk_ .</span><span class="sxs-lookup"><span data-stu-id="33756-115">Release the pointer pointed to by the  _lppUnk_ parameter.</span></span> 
    
5. <span data-ttu-id="33756-116">Chame [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar o próximo grupo de linhas.</span><span class="sxs-lookup"><span data-stu-id="33756-116">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the next group of rows.</span></span> 
    
7. <span data-ttu-id="33756-117">Libere a tabela de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="33756-117">Release the contents table.</span></span>
    

