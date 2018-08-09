---
title: Sobre o último tempo de atualização de um catálogo de endereços offline
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: d8c554c5-89ac-9b32-5561-8d8178d2525a
description: Um endereço catálogo Offline (OAB) fornece os usuários do Outlook no access estado desconectado às informações de diretório da lista de endereços Global (GAL) e de outros catálogos de endereços.
ms.openlocfilehash: b1e3ff012606615e5e962c400f86ab5ee2fbed83
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765810"
---
# <a name="about-the-last-update-time-of-an-offline-address-book"></a>Sobre o último tempo de atualização de um catálogo de endereços offline

Um endereço catálogo Offline (OAB) fornece os usuários do Outlook no access estado desconectado às informações de diretório da lista de endereços Global (GAL) e de outros catálogos de endereços. É uma cópia de um catálogo de endereços que o Outlook baixou de um servidor Exchange para fornecer acesso offline.
  
Os administradores do Exchange podem escolher quais catálogos de endereços a serem disponibilizadas para os usuários que trabalham offline. Para criar uma cópia de um catálogo de endereços, Exchange gera novos arquivos OAB, compacta os arquivos e coloca-los em um compartilhamento de local. Dependendo de como o Outlook estiver configurado, o Outlook baixa os arquivos OAB a partir da Web ou de uma pasta pública em um computador cliente para usar em um estado desconectado. Outlook periodicamente verifica e baixa atualizações do OAB.
  
Soluções do Outlook que deseja fornecer aos usuários acesso offline a um OAB, talvez seja necessário descobrir quando o OAB da última atualização do Exchange server. Para localizar a hora da última atualização de um OAB, soluções podem usar a seguinte entrada no registro do Windows: **HKCU\Software\Microsoft\Exchange\Exchange Provider\OAB hora da última modificação**. O tipo de entrada do registro é **REG_BINARY**. Os dados são 8 bytes de tamanho. Você pode converter os dados para uma estrutura [FILETIME](http://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx) de 64 bits especificando um valor de tempo Universal Coordenado (UTC) que o Outlook última baixou os arquivos OAB do Exchange server para o computador cliente. 
  
## <a name="see-also"></a>Confira também

- [Gerenciando catálogos de Endereços Offline](http://msdn.microsoft.com/library/b7f26eca-b93b-4834-ba50-11febdefbb18.aspx)

