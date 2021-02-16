---
title: Sobre a API do serviço de disponibilidade
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 17c5e44e-ae56-8de7-3579-90171d996411
description: A API de Livre/Ocupado permite que os provedores de email forneçam informações de status de livre/ocupado para contas de usuário especificadas dentro de um intervalo de tempo especificado.
ms.openlocfilehash: 1bcd191b57238771ede6f035216fe3997e82e03a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433756"
---
# <a name="about-the-freebusy-api"></a>Sobre a API do serviço de disponibilidade

A API de Livre/Ocupado permite que os provedores de email forneçam informações de status de livre/ocupado para contas de usuário especificadas dentro de um intervalo de tempo especificado. O status de livre/ocupado de um bloco de tempo no calendário de um usuário é um dos seguintes: fora do escritório, ocupado, provisório ou livre.
  
## <a name="create-a-freebusy-provider"></a>Criar um provedor de informações de livre/ocupado

Para fornecer informações de livre/ocupado aos usuários de email, um provedor de email cria um provedor de informações de livre/ocupado e o registra no Outlook. O provedor de informações de livre/ocupado deve implementar as interfaces a seguir. Observe que um número de membros nessas interfaces não é suportado e deve retornar os valores de retorno especificados. Em particular, a API de Livre/Ocupado não dá suporte a acesso de gravação a informações de livre/ocupado e delegar acesso a contas.
  
- [IFreeBusySupport](ifreebusysupport.md) — Essa interface dá suporte à especificação de interfaces que acessam dados de livre/ocupado para usuários especificados. Ele usa [FBUser](fbuser.md) para identificar um usuário. 
    
- [IFreeBusyData](ifreebusydata.md) — essa interface obtém e define um intervalo de tempo para um determinado usuário e retorna uma interface para enumerar blocos de informações de livre/ocupado dentro desse intervalo de tempo. Ele usa o tempo relativo para obter e definir esse intervalo de tempo. Para obter mais informações, [consulte Usar o tempo relativo para acessar dados de livre/ocupado.](how-to-use-relative-time-to-access-free-busy-data.md)
    
- [IEnumFBBlock](ienumfbblock.md) — Essa interface dá suporte ao acesso e à enumeração de blocos de informações de livre/ocupado para um usuário dentro de um intervalo de tempo. 
    
   > [!NOTE]
   > Uma enumeração contém blocos de livre/ocupado que indicam o status de livre/ocupado dos períodos de tempo no calendário de um usuário, dentro de um intervalo de tempo (especificado por [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)). Itens em um calendário, como compromissos e solicitações de reunião, blocos de formulário na enumeração. Os itens adjacentes entre si no calendário e que têm o mesmo status de livre/ocupado são combinados para formar um único bloco. Um período de tempo livre em um calendário também forma um bloco. Portanto, dois blocos consecutivos em uma enumeração não teriam o mesmo status de livre/ocupado. Esses blocos não se sobrepõem no tempo. Quando há itens sobrepostos em um calendário, o Outlook mescla esses itens para formar blocos de disponibilidade não sobrepostos na enumeração com base nesta ordem de prioridade: ausência temporária, ocupado, provisório. 
  
Para registrar o provedor de informações de livre/ocupado com o Outlook, o provedor de email deve fazer o seguinte:
  
1. Registre o provedor de informações de livre/ocupado com COM, fornecendo um CLSID que permite acesso à implementação do provedor **de IFreeBusySupport**. 
    
2. Let Outlook know that the free/busy provider exists by setting the following key (where `<xx.x>` represents the version of Outlook) in the system registry: 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\<xx.x>\Outlook\SchedulingInformation\FreeBusySupport`
    
   For example, if the transport provider is SMTP, to register the provider with Microsoft Outlook 2010, set the following key to the data in the following table: 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook\SchedulingInformation\FreeBusySupport`
    
   |Nome |Tipo |Valor |
   |:-----|:-----|:-----|
   |SMTP  |REG_SZ  |{CLSID para a respectiva implementação de IFreeBusySupport}  |
   
   Neste cenário, o Outlook cria a classe COM em coautoria e a usa para recuperar informações de livre/ocupado para qualquer usuário de email SMTP.
    
Para dar suporte a um agendador de endereços e provedor de transporte que use um tipo de entrada de endereço diferente de SMTP, altere  *o Nome* de acordo. 
  
> [!NOTE]
> Durante a instalação, os provedores de informações de livre/ocupado devem verificar se já existe uma configuração do Registro para o mesmo tipo de entrada de endereço. Se isso acontecer, o provedor de informações de livre/ocupado deverá substituir o provedor atual por esse tipo de entrada de endereço e restaurá-lo quando ele for desinstalado. No entanto, se um usuário tiver instalado mais de um provedor de informações para o mesmo tipo de entrada de endereço, o usuário deverá desinstalar esses provedores na ordem inversa da instalação (ou seja, sempre desinstalar o provedor mais recente). Caso contrário, o Registro poderá apontar para um provedor que já tenha sido desinstalado. 
  
## <a name="api-components"></a>Componentes da API

A API de Livre/Ocupado inclui os seguintes componentes:
  
### <a name="definitions"></a>Definições

- [Constantes (API do serviço de disponibilidade)](constants-free-busy-api.md)
    
### <a name="data-types"></a>Tipos de dados

- [FBBlock_1](fbblock_1.md)
- [FBStatus](fbstatus.md)
- [FBUser](fbuser.md)
    
### <a name="interfaces"></a>Interfaces

- [IEnumFBBlock](ienumfbblock.md)
- [IFreeBusyData](ifreebusydata.md)
- [IFreeBusySupport](ifreebusysupport.md)
    

