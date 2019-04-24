---
title: Sobre a alteração programática da base de calendários para o horário de verão
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 38b342d9-ab10-04b6-5490-9a45f847a60f
description: Neste tópico, este período entre a primavera e o outono é denominado como período DST.
ms.openlocfilehash: 8d9a0ffda89ee9d8847cde59181747588a50e947
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316951"
---
# <a name="about-rebasing-calendars-programmatically-for-daylight-saving-time"></a>Sobre a alteração programática da base de calendários para o horário de verão

Muitos países/regiões observam o horário verão (DST) adiantando os relógios para que a luz do dia se prolongue nos finais de tarde. Isso geralmente é feito adiantando o relógio em uma hora na primavera e retrocedendo em uma hora no outono. Neste tópico, este período entre a primavera e o outono é denominado como período DST. A maioria dos países/regiões tem suas próprias regulações para o início e término do horário de verão. As datas do período de horário de verão podem mudar de um ano para outro, e os usuários precisam atualizar seus calendários do Microsoft Outlook sempre que mudam as normas do horário de verão. 
  
Se usar uma versão do Windows como Windows Vista ou posterior, ou se tiver a atualização automática do Windows habilitada, você não será afetado pela alteração do horário de verão. Caso contrário, você deve instalar as atualizações do horário de verão para Windows. Independentemente das atualizações serem instaladas automaticamente, em seu nome pelo departamento de TI ou por você mesmo como usuário doméstico, alguns compromissos existentes que acontecem durante o período do horário de verão podem exibir horários incorreto depois da instalação das atualizações do DST para Windows. Isso acontece tanto para compromissos recorrentes quanto para compromissos de ocorrência única. Você deve atualizar esses compromissos para exibi-los corretamente no Outlook, Outlook Web App e em aplicativos baseados em Objetos de Dados de Colaboração (CDO). A ação de atualizar compromissos exibidos incorretamente nos calendários devido ao horário de verão é conhecida como a alteração programática da base de calendários.
  
O Outlook fornece ferramentas para usuários, e o Exchange Server fornece ferramentas para que os administradores façam alterações programáticas nos calendários. O Outlook fornece a Ferramenta de Atualização de Dados de Fuso Horário para usuários do Outlook. Com essa ferramenta, os usuários podem atualizar seus próprios calendários. O Exchange Server fornece a Ferramenta de Atualização do Calendário do Exchange, que ajuda os administradores a evitar dificuldades resultantes do uso da ferramenta Outlook com abrangência de todos os usuários, e a ter certeza de que cada usuário execute a ferramenta Outlook corretamente.
  
Além de depender dos usuários para executar a Ferramenta de Atualização de Dados de Fuso Horário, ou dos administradores para executar a Ferramenta de Atualização do Calendário do Exchange, os desenvolvedores terceiros de software de clientes MAPI podem baixar uma DLL chamada Tzmovelib.dll. Ao usar este montagem, os desenvolvedores podem usar as mesmas APIs que o Outlook e o Exchange Server usam em suas ferramentas de alteração programática de calendários. 

A lista a seguir mostra as APIs de alteração programática de calendários:
  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)
    
- [IOlkApptRebaser](iolkapptrebaser.md)
    
- [IOlkApptRebaser::BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)
    
- [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)
    
- [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)
    
- [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)
    
- [PidLidAppointmentTimeZoneDefinitionEndDisplay](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx)
    
- [PidLidAppointmentTimeZoneDefinitionRecur](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)
    
- [PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx)
    
- [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx)
    
- [RebaseTaskComplete](rebasetaskcomplete.md)
    
- [RebaseTaskProgress](rebasetaskprogress.md)
    
- [TZDEFINITION](tzdefinition.md)
    
- [TZREG](tzreg.md)
    
- [TZRULE](tzrule.md)
    
Para escrever uma ferramenta de alteração programática de compromissos usado as APIs de alteração programática de calendários, você pode usar o seguinte procedimento:
  
1. Use **IOlkApptRebaser::BeginEnumerateAppointments** e **IOlkApptRebaser::EndEnumerateAppointments**para localizar compromissos que são candidatos à alteração programática. Se necessário, apresente informações para habilitar o usuário a decidir em quais compromissos fazer a alteração programática. Alternativamente, use o MAPI ou o Modelo de Objeto do Outlook para examinar as informações de hora e recorrência de um compromisso analisando as propriedades **PidLidAppointmentTimeZoneDefinitionStartDisplay**, **PidLidAppointmentTimeZoneDefinitionEndDisplay** e **PidLidAppointmentTimeZoneDefinitionRecur**. 
    
2. Use **HrCreateApptRebaser**, **IOlkApptRebaser::BeginRebaseAppointments** e **IOlkApptRebaser::EndRebaseAppointments** para alterar o compromisso. 
    
Para obter a montagem Tzmovelib.dll, baixe o instalador redistribuível OutlookTimeZoneMoveLibRedist.exe e o arquivo-cabeçalho Tzmovelib.h em [Outlook 2010: Instalador Redistribuível de Referências Auxiliares e Arquivo-Cabeçalho para Alteração Programática de Calendários](https://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b). Esse download funciona para o Outlook 2010 e versões posteriores do Outlook. O OutlookTimeZoneMoveLibRedist.exe instala o arquivo de montagem Tzmovelib.dll em C:\Program Files\MsExTmz. Observe que os aplicativos de alteração programática de calendários de terceiros podem redistribuir apenas o instalador, OutlookTimeZoneMoveLibRedist.exe, e não devem redistribuir a montagem, Tzmovelib.dll, ou quaisquer outros componentes extraídos separadamente do instalador.
  
## <a name="see-also"></a>Confira também

- [Sobre TZDEFINITION persistente em um fluxo para confirmar uma propriedade binária](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)
- [Analisar um fluxo de uma propriedade binária para ler a estrutura TZDEFINITION](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [Analisar um fluxo de uma propriedade binária para ler a estrutura TZREG](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
- [Ler propriedades de fuso horário de um compromisso](how-to-read-time-zone-properties-from-an-appointment.md)
- [Centro de Ajuda e Suporte do Horário de Verão](https://support.microsoft.com/gp/cp_dst)
- [Como lidar com o horário de verão usando a Ferramenta de Atualização de Calendários do Exchange](https://support.microsoft.com/kb/941018)
- [Como resolver alterações de fuso horário usando a Ferramenta de Atualização de Dados de Fuso Horário do Microsoft Office Outlook](https://support.microsoft.com/kb/931667)

