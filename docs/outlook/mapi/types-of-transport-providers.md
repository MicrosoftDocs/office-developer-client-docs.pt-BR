---
title: Tipos de provedores de transporte
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 772ecab1-7e91-415b-bae8-af8ffb7b7ed9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4a0ab660b8df2fb32f21f9bc93932a9187c37b7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770636"
---
# <a name="types-of-transport-providers"></a>Tipos de provedores de transporte

  
  
**Aplica-se a**: Outlook 
  
Todos os provedores de transporte oferecem suporte a uma variedade de recursos padrão, como:
  
- Fornecimento de segurança adequadas para o sistema de mensagens subjacente.
    
- Enviando e recebendo mensagens do sistema de mensagens subjacente.
    
- Expondo os tipos de endereço os provedores de transporte oferecem suporte para que o spooler MAPI e aplicativos cliente podem usá-las apropriadamente.
    
- Aceitando entrega a destinatários específicos.
    
Além disso, o MAPI suporta dois tipos de especializados de provedores de sistemas de mensagens específicos.
  
|**Tipo de transporte**|**Funcionalidade adicionada**|
|:-----|:-----|
|Transporte remoto  <br/> |Permite a interoperabilidade com clientes conectados remotamente.  <br/> |
|Transporte TNEF  <br/> |Permite que as propriedades MAPI seja preservado em sistemas que não têm suporte-los de mensagens.  <br/> |
   
TNEF transportes são usados para traduzir mensagens entre sistemas de mensagens que oferecem suporte a diferentes conjuntos de propriedades MAPI. Usam o TNEF transportes MAPI [ITnef: IUnknown](itnefiunknown.md) interface para converter todas as propriedades que o sistema de destino não pode representar diretamente em um fluxo de dados binários que pode ser anexado à mensagem. Mais tarde, transporte de outro TNEF pode usar **ITnef** para decodificar o fluxo de dados e fazer as propriedades MAPI originais disponível para aplicativos cliente. Além disso, o suporte TNEF é necessário se o seu transporte precisa suportar classes de mensagem personalizada. Para obter informações sobre como implementar transportes TNEF, consulte [desenvolvendo um provedor de transporte TNEF-Enabled](developing-a-tnef-enabled-transport-provider.md).
  
Se seu provedor de transporte não for um desses tipos, você precisará implementá-lo com as funções básicas de MAPI e funções de rede disponíveis em sua plataforma de destino.
  

