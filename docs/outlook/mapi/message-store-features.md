---
title: Recursos do repositório de mensagens
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d9167cd2-fc88-46b1-9a26-151955fb606c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7e99d9d2e1289ed98ba659e97b05c8ea6d891a74
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581808"
---
# <a name="message-store-features"></a>Recursos do repositório de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Provedores de armazenamento de mensagem são mais complexos que outros provedores de serviços MAPI em que os provedores de armazenamento de mensagem obtêm uma ampla gama de recursos opcionais, que eles podem implementar. A lista de recursos necessários para um provedor de armazenamento de mensagens é relativamente curta. No entanto, um provedor de armazenamento de mensagem típica dará suporte a um número de recursos opcionais, porque muitos dos recursos opcionais são muito úteis ou exigido pela maioria dos clientes MAPI. A tabela a seguir lista os principais recursos que os provedores de armazenamento de mensagens podem implementar e se cada recurso é obrigatório ou opcional para mensagens de todos os provedores de armazenamento e provedores de armazenamento de mensagem padrão.
  
|**Recurso**|**All**|**Padrão**|
|:-----|:-----|:-----|
|Fornecimento de status com a tabela de status MAPI.  <br/> |Required  <br/> |Required  <br/> |
|Implementando objetos folder.  <br/> |Required  <br/> |Required  <br/> |
|Implementando objetos de mensagem.  <br/> |Required  <br/> |Required  <br/> |
|Fornecimento de relatórios de leitura e nonread.  <br/> |Required  <br/> |Required  <br/> |
|Fornecendo uma interface de andamento.  <br/> |Required  <br/> |Required  <br/> |
|Fornecendo uma interface de configuração.  <br/> |Required  <br/> |Required  <br/> |
|Tabelas de conteúdo associado de suporte para suporte de formulário e modo de exibição.  <br/> |Opcional  <br/> |Opcional  <br/> |
|Provedor de armazenamento de envio de mensagens com a mensagem.  <br/> |Opcional  <br/> |Obrigatório  <br/> |
|Recebendo mensagens com o provedor de armazenamento de mensagem.  <br/> |Opcional  <br/> |Obrigatório  <br/> |
|Dando suporte a anexos de mensagens.  <br/> |Opcional  <br/> |Opcional  <br/> |
|Dando suporte a Rich Text Format para mensagens.  <br/> |Opcional  <br/> |Opcional  <br/> |
|Fornecimento de notificações.  <br/> |Opcional  <br/> |Opcional  <br/> |
|Pesquisas de suporte.  <br/> |Opcional  <br/> |Opcional  <br/> |
|Suporte hermeticamente acoplada provedores de repositório/transporte de mensagem.  <br/> |Opcional  <br/> |Opcional  <br/> |
|Dando suporte a não reutilização de identificadores de entrada.  <br/> |Opcional  <br/> |Opcional  <br/> |
   
Muitos dos recursos opcionais podem ser divulgados para MAPI e propriedade de **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) do objeto de armazenamento de aplicativos do cliente, definindo diversos sinalizadores na mensagem. Os recursos necessários não têm sinalizadores associados a eles. **PR_STORE_SUPPORT_MASK** é necessário no armazenamento de mensagens, pasta e objetos de mensagem. 
  
## <a name="see-also"></a>Confira também



[Desenvolver um provedor do repositório de mensagens MAPI](developing-a-mapi-message-store-provider.md)

