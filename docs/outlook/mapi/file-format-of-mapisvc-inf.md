---
title: Formato de arquivo do Mapisvc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b48eda17-83a8-4dc4-85c8-4ca827d13d25
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 47b698eb12577442e5b2d9ea9ecae3e8a13e402b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766545"
---
# <a name="file-format-of-mapisvcinf"></a>Formato de arquivo do Mapisvc

**Aplica-se a**: Outlook 
  
O arquivo Mapisvc atua como o banco de dados central para obter informações de configuração de serviço de mensagem MAPI. Mapisvc contém informações sobre cada um dos serviços de mensagem instalados na estação de trabalho, informações sobre os provedores de serviço que pertencem a cada serviço de mensagem e informações sobre o subsistema de MAPI. Mapisvc é a principal fonte de informações de perfis. Ou seja, quando um novo perfil está sendo construído ou um existente modificado, as informações relevantes para cada serviço de mensagem ou provedor de serviços é copiado do Mapisvc. 
  
Mapisvc é dividido em seções hierárquicas vinculadas:
  
1. Seção que contém informações que se aplicam a todos os perfis. Esta seção possui três partes:
    
   - Seção **[serviços]** , oferecendo links para cada um da mensagem subsequente seções de serviço. 
    
   - Seção **[Help File Mappings]** , que contém informações sobre. Arquivos HLP fornecidos pelos serviços de mensagem. 
    
   - Seção **[Services padrão]** , listando os serviços de mensagem que compõem uma instalação padrão. 
    
2. Seção que contém informações que se aplicam aos serviços de mensagem individual. Entradas nestas seções fornecem links para seções do provedor de serviço subsequentes.
    
3. Seção que contém informações que se aplicam a provedores de serviços individuais em um serviço de mensagem.
    
A ilustração a seguir mostra a organização de um arquivo Mapisvc típico. Há três serviços de mensagem: AB, MsgService e MS. O nome na parte lateral direita do sinal de igual para cada serviço de mensagem é o nome para exibição do serviço. Cada serviço de mensagem tem sua própria seção em outro local do arquivo que é vinculado a uma ou mais seções do provedor de serviço. Não há uma seção de provedor de serviço para cada provedor de serviço que pertence ao serviço de mensagem. Os serviços de mensagem AB e MS são serviços único provedor, enquanto os três provedores de serviços pertencem ao serviço MsgService.
  
**MapiSvc.inf file organization**
  
![Organização de arquivo Mapisvc] (media/amapi_30.gif "Organização de arquivo Mapisvc")
  
MAPI fornece uma versão estrutural do arquivo Mapisvc que contém as entradas para o subsistema MAPI. Cada implementador de serviço de mensagem adiciona entradas que são apropriadas para seu serviço e os provedores de serviços que pertencem ao seu serviço. Algumas das entradas são necessárias, enquanto outros são opcionais. Por exemplo, o MAPI requer que você especifique o nome e caminho de cada um dos provedores de serviços em seu serviço de mensagem. Sem essas informações, eles não podem ser carregados.
  
Você pode adicionar informações obrigatórios e opcionais nas seções para seu serviço de mensagem e/ou as seções do provedor de serviço. Onde você coloca as informações que descrevem o seu serviço de mensagem depende do número de provedores de serviço no serviço. Porque essas informações se aplicam a cada provedor de serviço no serviço, você deve torná-lo acessível a todos os provedores. Armazená-lo na seção de serviço de mensagem, a opção preferida, ou em todas as seções do provedor de serviço. Armazenar informações de uma vez para evitar replicações desnecessárias e a necessidade de guardar diversas cópias sincronizados.
  
Se sua mensagem for um serviço único provedor, armazene todas as informações de serviço de mensagem na seção para o provedor de serviço, em vez de na seção para o serviço. Acessando a seção de provedor de serviço é mais rápido e mais direto do que o acesso a seção de serviço de mensagem. 
  
Armazene apenas dados de configuração pública no arquivo Mapisvc. Informação privada ou requer proteção extra, como senhas ou outras credenciais, não deve ser incluída neste arquivo. Em vez disso, optar por tanto não armazenam informações desse tipo nisso ou mantê-los no perfil como propriedades seguras. Propriedades protegidas têm recursos de proteção interna, como criptografia.
  

