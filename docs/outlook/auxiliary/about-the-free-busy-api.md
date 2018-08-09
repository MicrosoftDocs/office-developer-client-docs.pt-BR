---
title: Sobre a API do serviço de disponibilidade
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 17c5e44e-ae56-8de7-3579-90171d996411
description: A API de Free/Busy permite que os provedores de email fornecer informações de status livre/ocupado para contas de usuário especificado dentro de um intervalo de tempo especificado.
ms.openlocfilehash: 8b1559173297fbde9930b6f8f7fbc74f176273da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765792"
---
# <a name="about-the-freebusy-api"></a>Sobre a API do serviço de disponibilidade

A API de Free/Busy permite que os provedores de email fornecer informações de status livre/ocupado para contas de usuário especificado dentro de um intervalo de tempo especificado. O status livre/ocupado de um bloco de horário no calendário do usuário é um dos seguintes: fora do escritório, ocupado, provisório ou livre.
  
## <a name="create-a-freebusy-provider"></a>Criar um provedor de livre/ocupado

Para fornecer informações de livre/ocupado para usuários de email, um provedor de email cria um provedor de livre/ocupado e registra-lo com o Outlook. O provedor de livre/ocupado deve implementar estas interfaces. Observe que um número de membros nessas interfaces não é suportado e deve retornar que valores de retorno especificado. Especificamente, a API Free/Busy não oferece suporte para acesso de gravação para as informações de disponibilidade e delegar acesso às contas.
  
- [IFreeBusySupport](ifreebusysupport.md) — essa interface suporta a especificação das interfaces que acessam dados livre/ocupado para usuários especificados. Ele usa [FBUser](fbuser.md) para identificar um usuário. 
    
- [IFreeBusyData](ifreebusydata.md) — essa interface obtém e define um intervalo de tempo para um determinado usuário e retorna uma interface para enumerar os blocos de informações de disponibilidade de dados dentro deste intervalo de tempo. Ele usa o tempo relativo para obter e definir esse intervalo de tempo. Para obter mais informações, consulte [tempo relativo para acessar informações de disponibilidade de dados de uso](how-to-use-relative-time-to-access-free-busy-data.md).
    
- [IEnumFBBlock](ienumfbblock.md) — essa interface suporta acessando e enumerando blocos de informações de disponibilidade de dados de um usuário em um intervalo de tempo. 
    
   > [!NOTE]
   > Uma enumeração contém blocos de livre/ocupado que indicam o status livre/ocupado de períodos de tempo no calendário do usuário, dentro de um intervalo de tempo (especificado por [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)). Itens em um calendário, como compromissos e solicitações de reunião, blocos de formulário na enumeração. Itens que são adjacentes uns aos outros no calendário e têm o mesmo status livre/ocupado são combinados para um único bloco do formulário. Um período livre de tempo em um calendário também um bloco de formulários. Portanto, não há dois blocos consecutivos em uma enumeração teria o mesmo status livre/ocupado. Esses blocos não se sobreponham em tempo. Quando houver sobreposição de itens em um calendário, o Outlook mescla desses itens para formar não sobrepostos blocos de livre/ocupado na enumeração com base nesta ordem de precedência: fora do escritório, ocupado, provisório. 
  
Para registrar o provedor de informações de disponibilidade com o Outlook, o provedor de email deve fazer o seguinte:
  
1. Registre o provedor de livre/ocupado com, fornecendo um CLSID que permite o acesso a implementação do provedor de **IFreeBusySupport**. 
    
2. Permitir que o Outlook saibam a existência de provedor de livre/ocupado, definindo a seguinte chave (onde `<xx.x>` representa a versão do Outlook) no registro do sistema: 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\<xx.x>\Outlook\SchedulingInformation\FreeBusySupport`
    
   Por exemplo, se o provedor de transporte for SMTP, para registrar o provedor com o Microsoft Outlook 2010, defina a seguinte chave para os dados na tabela a seguir: 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook\SchedulingInformation\FreeBusySupport`
    
   |Name |Tipo |Value |
   |:-----|:-----|:-----|
   |SMTP  |REG_SZ  |{CLSID referente a respectiva implementação da IFreeBusySupport}  |
   
   Neste cenário, o Outlook co cria a classe COM e o utiliza para recuperar informações de disponibilidade para os usuários de email SMTP.
    
Para oferecer suporte a um provedor de transporte e o catálogo de endereço que usam um tipo de endereço de entrada que não seja o SMTP, altere o *nome* de acordo. 
  
> [!NOTE]
> Durante a instalação, provedores de livre/ocupado devem verificar se uma configuração de registro para o mesmo tipo de entrada de endereço já existe. Se contiver, o provedor de livre/ocupado deve substituir o provedor atual para esse tipo de entrada de endereço e restaure desse provedor quando ele é desinstalado. No entanto, se um usuário tiver instalado mais de um provedor de livre/ocupado para o mesmo tipo de entrada de endereço, o usuário deve desinstalar esses provedores na ordem inversa da instalação (ou seja, desinstale sempre o provedor mais recente). Caso contrário, o registro pode apontar para um provedor que já está desinstalado. 
  
## <a name="api-components"></a>Componentes de API

A API Free/Busy inclui os seguintes componentes:
  
### <a name="definitions"></a>Definições

- [Constantes (API de livre/ocupado)](constants-free-busy-api.md)
    
### <a name="data-types"></a>Tipos de dados

- [FBBlock_1](fbblock_1.md)
- [FBStatus](fbstatus.md)
- [FBUser](fbuser.md)
    
### <a name="interfaces"></a>Interfaces

- [IEnumFBBlock](ienumfbblock.md)
- [IFreeBusyData](ifreebusydata.md)
- [IFreeBusySupport](ifreebusysupport.md)
    

