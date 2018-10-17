---
title: Sobre o último tempo de atualização de um catálogo de endereços offline
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: d8c554c5-89ac-9b32-5561-8d8178d2525a
description: O OAB (Catálogo de Endereços Offline) oferece aos usuários do Outlook acesso em estado desconectado às informações de diretório da GAL (Lista de Endereços Globais) e de outras listas de endereços.
ms.openlocfilehash: 3374f87cd62d46a80ed823bff0516115a58c155c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392281"
---
# <a name="about-the-last-update-time-of-an-offline-address-book"></a>Sobre o último tempo de atualização de um catálogo de endereços offline

O OAB (Catálogo de Endereços Offline) oferece aos usuários do Outlook acesso em estado desconectado às informações de diretório da GAL (Lista de Endereços Globais) e de outras listas de endereços. É uma cópia de um Catálogo de Endereços que o Outlook baixou de um servidor Exchange para fornecer acesso offline.
  
Os administradores do Exchange podem escolher quais Catálogos de Endereços disponibilizar para os usuários que trabalham offline. Para criar uma cópia de um Catálogo de Endereços, o Exchange gera novos arquivos OAB, compacta-os e coloca-os em um compartilhamento local. Dependendo da configuração do Outlook, o Outlook baixa os arquivos OAB da Web ou de uma Pasta Pública em um computador cliente para usar no estado desconectado. O Outlook verifica periodicamente e baixa atualizações do OAB.
  
Soluções do Outlook que querem proporcionar aos usuários acesso offline a um OAB podem precisar descobrir quando o OAB foi atualizado pela última vez do servidor Exchange. Para localizar a hora da última atualização de um OAB, as soluções podem usar a entrada a seguir no registro do Windows: **HKCU\Software\Microsoft\Exchange\Exchange Provider\OAB Last Modified Time**. O tipo desta entrada do registro é **REG_BINARY**. Os dados têm 8 bytes de tamanho. Você pode converter os dados para uma estrutura [FILETIME](https://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx) de 64 bits especificando o valor do Tempo Universal Coordenado (UTC) no qual o Outlook baixou os arquivos OAB do servidor Exchange pela última vez para o computador cliente. 
  
## <a name="see-also"></a>Confira também

- [Gerenciar Catálogos de Endereços Offline](https://msdn.microsoft.com/library/b7f26eca-b93b-4834-ba50-11febdefbb18.aspx)

