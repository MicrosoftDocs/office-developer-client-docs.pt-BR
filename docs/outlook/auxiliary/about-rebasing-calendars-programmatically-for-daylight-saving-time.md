---
title: Sobre a alteração da base calendários programaticamente para horário de verão
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 38b342d9-ab10-04b6-5490-9a45f847a60f
description: Neste tópico, esse período entre a mola e queda é conhecido como o período de horário de verão.
ms.openlocfilehash: 4787b2143b3f5d1f0400524f0da82e19e2cbed8a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765787"
---
# <a name="about-rebasing-calendars-programmatically-for-daylight-saving-time"></a>Sobre a alteração da base calendários programaticamente para horário de verão

Vários países observam o horário de verão (DST) avançando relógios para que as noites tenham mais horário de verão. Normalmente, isso é feito definindo o relógio uma hora com antecedência no primeiro semestre e definindo o relógio uma hora de volta no terceiro trimestre. Neste tópico, esse período entre a mola e queda é conhecido como o período de horário de verão. A maioria dos países têm suas próprias normas para quando o horário de verão começa e termina. As datas do período de horário de verão podem alterar todos os anos, e os usuários devem atualizar seu calendário do Microsoft Outlook toda vez que as normas de horário de verão alterem. 
  
Se você usar uma versão do Windows que é o Windows Vista ou posterior, ou ter ativada de atualização automática do Windows, você não pode ser afetado pela alteração no horário de verão. Caso contrário, você deve instalar atualizações de horário de verão do Windows. Independentemente se as atualizações são instaladas automaticamente, em seu nome por um departamento de TI ou por si mesmo como um usuário residencial, alguns existentes compromissos que ocorrem durante o período de horário de verão podem exibir incorretos horários depois que as atualizações de horário de verão para Windows estão instaladas . Isso é verdadeiro para compromissos recorrentes e instância única. Você deve atualizar esses compromissos para exibi-las corretamente no Outlook, no Outlook Web App e em aplicativos baseados em Collaboration Data Objects (CDO). A atualização de compromissos exibidos incorretamente em calendários por causa do horário de verão é conhecida como a alteração da Base de calendários.
  
O Outlook oferece ferramentas para usuários e Exchange Server fornece ferramentas para que os administradores calendários de alterar. O Outlook oferece a ferramenta de atualização de dados de fuso horário para usuários do Outlook. Com essa ferramenta, os usuários podem atualizar seus próprios calendários. Exchange Server fornece a ferramenta de atualização de calendário do Exchange que ajuda os administradores para evitar dificuldades resultantes de implantar a ferramenta de Outlook amplamente a todos os usuários e para certificar-se de que cada usuário executa a ferramenta de Outlook corretamente.
  
Além de contar com os usuários possam executar a ferramenta de atualização de dados de fuso horário ou administradores para executar a ferramenta de atualização de calendário do Exchange, desenvolvedores de software de cliente MAPI de terceiros podem baixar uma DLL, Tzmovelib.dll. Usando este assembly, os desenvolvedores podem usar as APIs mesmas que usam o Outlook e Exchange Server no seu calendário, a alteração da Base de ferramentas. 

A lista a seguir mostra o calendário a alteração da Base de APIs:
  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)
    
- [IOlkApptRebaser](iolkapptrebaser.md)
    
- [IOlkApptRebaser::BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)
    
- [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)
    
- [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)
    
- [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)
    
- [PidLidAppointmentTimeZoneDefinitionEndDisplay](http://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx)
    
- [PidLidAppointmentTimeZoneDefinitionRecur](http://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)
    
- [PidLidAppointmentTimeZoneDefinitionStartDisplay](http://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx)
    
- [PidLidTimeZoneStruct](http://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx)
    
- [RebaseTaskComplete](rebasetaskcomplete.md)
    
- [RebaseTaskProgress](rebasetaskprogress.md)
    
- [TZDEFINITION](tzdefinition.md)
    
- [TZREG](tzreg.md)
    
- [TZRULE](tzrule.md)
    
Para escrever uma ferramenta de REBASE de compromisso usando o calendário a alteração da Base de APIs, você pode usar o procedimento a seguir:
  
1. Use **IOlkApptRebaser::BeginEnumerateAppointments** e **IOlkApptRebaser::EndEnumerateAppointments** para encontrar os compromissos que são candidatos para a alteração da base. Se necessário, apresentar informações para permitir que o usuário decidir quais compromissos alterar a. Como alternativa, use o MAPI ou o modelo de objeto do Outlook para examinar as informações de tempo e de recorrência de um compromisso ao analisar o **PidLidAppointmentTimeZoneDefinitionStartDisplay**, **PidLidAppointmentTimeZoneDefinitionEndDisplay**, e as propriedades de **PidLidAppointmentTimeZoneDefinitionRecur** . 
    
2. Use **HrCreateApptRebaser**, **IOlkApptRebaser::BeginRebaseAppointments**e **IOlkApptRebaser::EndRebaseAppointments** para alterar o compromisso a. 
    
Para obter o assembly Tzmovelib.dll, baixe o instalador redistribuível de OutlookTimeZoneMoveLibRedist.exe e o arquivo de cabeçalho Tzmovelib.h no [Outlook 2010: instalador redistribuível de referência auxiliar e o arquivo de cabeçalho para a alteração da Base de calendários](http://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b) . Este download funciona para Outlook 2010 e versões posteriores do Outlook. OutlookTimeZoneMoveLibRedist.exe instala o arquivo de assembly Tzmovelib.dll em C:\Program Files\MsExTmz. Observe que os aplicativos de REBASE de calendário de terceiros podem redistribuir apenas o instalador, OutlookTimeZoneMoveLibRedist.exe e não devem redistribuir o assembly, Tzmovelib.dll ou qualquer outro extraída componentes separadamente do instalador.
  
## <a name="see-also"></a>Confira também

- [Sobre TZDEFINITION persistente em um fluxo para confirmar uma propriedade binária](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)
- [Analisar um fluxo de uma propriedade binária para ler a estrutura TZDEFINITION](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [Analisar um fluxo de uma propriedade binária para ler a estrutura TZREG](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
- [Ler as propriedades de fuso horário de um compromisso](how-to-read-time-zone-properties-from-an-appointment.md)
- [Horário de verão Centro de Ajuda e suporte](http://support.microsoft.com/gp/cp_dst)
- [Como resolver o horário de verão usando a ferramenta de atualização de calendário do Exchange](http://support.microsoft.com/kb/941018)
- [Como as alterações de fuso horário do endereço, usando a ferramenta de atualização de dados de fuso horário para Microsoft Office Outlook](http://support.microsoft.com/kb/931667)

