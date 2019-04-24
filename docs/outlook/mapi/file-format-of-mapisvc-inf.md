---
title: Formato de arquivo de MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
api_type:
- COM
ms.assetid: b48eda17-83a8-4dc4-85c8-4ca827d13d25
description: 'Última modificação: 23 de julho de 2011'
localization_priority: Priority
ms.openlocfilehash: 934bb491c0521b1d76d5400aac4728fbd34ba625
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334865"
---
# <a name="file-format-of-mapisvcinf"></a>Formato de arquivo de MapiSvc.inf

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O arquivo MapiSvc.inf atua como o banco de dados central para informações de configuração do serviço de mensagem do MAPI. MapiSvc.inf contém informações sobre cada um dos serviços de mensagem instalados na estação de trabalho, informações sobre os provedores de serviços que pertencem a cada serviço de mensagens e informações sobre o subsistema do MAPI. MapiSvc.inf é a principal fonte de informações para perfis. Ou seja, quando um novo perfil está sendo criado ou um existente é modificado, informações relevantes para cada serviço de mensagem ou provedor de serviços são copiadas do MapiSvc.inf. 
  
MapiSvc.inf é dividido em seções hierárquicas vinculadas:
  
1. Seção contendo informações que se aplicam a todos os perfis. Esta seção tem três partes:
    
   - A seção **[Services]** fornece links para cada uma das seções subsequentes do serviço de mensagens. 
    
   - A seção **[Help File Mappings]** contém informações sobre arquivos .HLP fornecidos pelos serviços de mensagens. 
    
   - A seção **[Default Services]** lista os serviços de mensagens que compõem uma instalação padrão. 
    
2. Seção contendo informações que se aplicam a serviços de mensagens individuais. As entradas nessas seções fornecem links para seções subsequentes de provedores de serviços.
    
3. Seção contendo informações que se aplicam a provedores de serviços individuais em um serviço de mensagens.
    
A ilustração a seguir mostra a organização de um arquivo MapiSvc.inf comum. Há três serviços de mensagens: AB, MsgService e MS. O nome no lado direito do sinal de igual para cada serviço de mensagem é o nome de exibição do serviço. Cada serviço de mensagens tem sua própria seção em outro local no arquivo e está vinculada a uma ou mais seções do provedor de serviços. Há uma seção de provedor de serviços para cada provedor de serviços que pertence ao serviço de mensagens. Os serviços de mensagens AB e MS são serviços de provedores únicos, enquanto três provedores de serviços pertencem ao serviço MsgService.
  
**MapiSvc.inf file organization**
  
![MapiSvc.inf file organization](media/amapi_30.gif "MapiSvc.inf file organization")
  
O MAPI fornece uma versão esquelética do arquivo MapiSvc.inf que contém as entradas para o subsistema do MAPI. Cada implementador de serviços de mensagens adiciona entradas que são apropriadas para seu serviço e para os provedores de serviços que pertencem ao seu serviço. Algumas entradas são necessárias, outras são opcionais. Por exemplo, o MAPI exige que você especifique o nome e o caminho de cada um dos provedores de serviço em seu serviço de mensagem. Sem essas informações, eles não poderão ser carregados.
  
Você pode adicionar informações obrigatórias e opcionais à seção do serviço de mensagens e/ou às seções do provedor de serviços. O local onde você coloca as informações que descrevem seu serviço de mensagens depende do número de provedores de serviços no serviço. Como essas informações se aplicam a cada provedor de serviços no serviço, você deve torná-las acessíveis a todos os provedores. Armazene-as na seção do serviço de mensagens, na opção preferida ou em todas as seções do provedor de serviços. Armazene informações apenas uma vez para evitar a replicação desnecessária e a necessidade de manter várias cópias sincronizadas.
  
Se o serviço de mensagens for um único provedor, armazene todas as informações do serviço de mensagens na seção do provedor de serviços, e não na seção do serviço. Acessar a seção do provedor de serviços é mais rápido e mais direto do que acessar a seção do serviço de mensagens. 
  
Armazene somente dados públicos de configuração no arquivo MapiSvc.inf. As informações privadas ou que exigem proteção extra, como senhas ou outras credenciais, não devem ser incluídas nesse arquivo. Em vez disso, opte por não armazenar informações desse tipo ou mantê-las no perfil como propriedades seguras. As propriedades seguras possuem recursos de proteção integrados, como criptografia.
  

