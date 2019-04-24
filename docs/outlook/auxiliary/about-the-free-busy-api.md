---
title: Sobre a API do serviço de disponibilidade
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 17c5e44e-ae56-8de7-3579-90171d996411
description: A API de disponibilidade permite que os provedores de email forneçam informações de status de disponibilidade para contas de usuário especificadas em um intervalo de tempo especificado.
ms.openlocfilehash: 1bcd191b57238771ede6f035216fe3997e82e03a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317007"
---
# <a name="about-the-freebusy-api"></a>Sobre a API do serviço de disponibilidade

A API de disponibilidade permite que os provedores de email forneçam informações de status de disponibilidade para contas de usuário especificadas em um intervalo de tempo especificado. O status de disponibilidade de um bloco de tempo no calendário de um usuário é um dos seguintes: fora do escritório, ocupado, provisório ou gratuito.
  
## <a name="create-a-freebusy-provider"></a>Criar um provedor de disponibilidade

Para fornecer informações de disponibilidade para usuários de email, um provedor de email cria um provedor de disponibilidade e o registra com o Outlook. O provedor de disponibilidade deve implementar as seguintes interfaces. Observe que não há suporte para vários membros nessas interfaces e deve retornar os valores de retorno especificados. Em particular, a API de disponibilidade não suporta acesso de gravação para informações de disponibilidade e acesso de representante a contas.
  
- [IFreeBusySupport](ifreebusysupport.md) – esta interface suporta a especificação de interfaces que acessam dados de disponibilidade para usuários específicos. Ele usa [FBUser](fbuser.md) para identificar um usuário. 
    
- [IFreeBusyData](ifreebusydata.md) – esta interface obtém e define um intervalo de tempo para um determinado usuário e retorna uma interface para enumerar blocos de disponibilidade de dados dentro desse intervalo de tempo. Ele usa o tempo relativo para obter e definir esse intervalo de tempo. Para obter mais informações, consulte [usar tempo relativo para acessar dados de disponibilidade](how-to-use-relative-time-to-access-free-busy-data.md).
    
- [IEnumFBBlock](ienumfbblock.md) — essa interface suporta o acesso e a enumeração de blocos de disponibilidade de dados para um usuário em um intervalo de tempo. 
    
   > [!NOTE]
   > Uma enumeração contém blocos de disponibilidade que indicam o status de disponibilidade dos períodos de tempo no calendário de um usuário, dentro de um intervalo de tempo (especificado por [IFreeBusyData:: EnumBlocks](ifreebusydata-enumblocks.md)). Itens em um calendário, como compromissos e solicitações de reunião, blocos de formulários na enumeração. Os itens que estão adjacentes entre si no calendário e têm o mesmo status de disponibilidade são combinados para formar um único bloco. Um período de tempo gratuito em um calendário também forma um bloco. Portanto, nenhum dois blocos consecutivos em uma enumeração teria o mesmo status de disponibilidade. Esses blocos não se sobrepõem no tempo. Quando há itens sobrepostos em um calendário, o Outlook mescla esses itens para formar blocos de disponibilidade não sobrepostos na enumeração com base nesta ordem de prioridade: ausência temporária, ocupado, provisório. 
  
Para registrar o provedor de disponibilidade com o Outlook, o provedor de email deve fazer o seguinte:
  
1. Registre o provedor de disponibilidade com com, fornecendo um CLSID que permite o acesso à implementação do **IFreeBusySupport**do provedor. 
    
2. Deixe o Outlook saber que existe o provedor de disponibilidade, definindo a seguinte chave (onde `<xx.x>` representa a versão do Outlook) no registro do sistema: 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\<xx.x>\Outlook\SchedulingInformation\FreeBusySupport`
    
   Por exemplo, se o provedor de transporte for SMTP, para registrar o provedor com o Microsoft Outlook 2010, defina a seguinte chave como os dados na tabela a seguir: 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook\SchedulingInformation\FreeBusySupport`
    
   |Nome |Tipo |Valor |
   |:-----|:-----|:-----|
   |SMTP  |REG_SZ  |{CLSID para a respectiva implementação de IFreeBusySupport}  |
   
   Neste cenário, o Outlook cria a classe COM e a usa para recuperar as informações de disponibilidade de qualquer usuário de email SMTP.
    
Para dar suporte a um catálogo de endereços e um provedor de transporte que usam um tipo de entrada de endereço diferente de SMTP, altere o *nome* de acordo. 
  
> [!NOTE]
> Durante a instalação, os provedores de disponibilidade devem verificar se uma configuração de registro para o mesmo tipo de entrada de endereço já existe. Se isso acontecer, o provedor de disponibilidade deverá substituir o provedor atual por esse tipo de entrada de endereço e restaurá-lo ao provedor quando ele for desinstalado. No enTanto, se um usuário tiver instalado mais de um provedor de disponibilidade para o mesmo tipo de entrada de endereço, o usuário deverá desinstalar esses provedores na ordem inversa como instalação (ou seja, sempre desinstalar o provedor mais recente). Caso contrário, o registro pode apontar para um provedor que já foi desinstalado. 
  
## <a name="api-components"></a>Componentes da API

A API de disponibilidade inclui os seguintes componentes:
  
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
    

