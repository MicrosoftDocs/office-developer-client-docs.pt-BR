---
title: Criar um controle ActiveX que pode associar-se a dados de formulário do InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a0d62047-bf08-9f70-de00-7f81ef1331f1
description: Você pode hospedar os Controles ActiveX nos formulários do InfoPath que podem ser abertos no InfoPath editor. Esses controles podem preexistentes (com algumas restrições) ou podem ser escritos especificamente para InfoPath.
ms.openlocfilehash: 70ac6a16b305403ffa99d8fe840a165913642f57
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300186"
---
# <a name="create-an-activex-control-that-can-bind-to-infopath-form-data"></a>Criar um controle ActiveX que pode associar-se a dados de formulário do InfoPath

Você pode hospedar os Controles ActiveX nos formulários do InfoPath que podem ser abertos no InfoPath editor. Esses controles podem preexistentes (com algumas restrições) ou podem ser escritos especificamente para InfoPath.
  
## <a name="write-an-activex-control"></a>Escrever um controle ActiveX

Como com outros controles no InfoPath, os controles ActiveX devem suportar interfaces de modelo COM (Component Object) existente:
  
- **IDispatch**
    
- **IPersistPropertyBag**
    
- **IPersistStreamInit**
    
- **IPropertyPage**
    
- **IObjectSafety**
    
- **IPropertyNotifySink**
    
- **IViewObject**
    
- **IOleObject**
    
- **IOleInPlaceObject**
    
Para que o InfoPath atualize propriedades no modelo de objeto de documento (DOM) no momento em que alterar no controle, o controle deve implementar o interfaces seguintes:
  
- **IConnectionPointContainer**
    
- **IEnumConnectionPoints**
    
- **IConnectionPoint**
    
- **IEnumConnections**
    
Além disso, há duas interfaces específicas do InfoPath COM que fornecem uma integração maior de controles:
  
- [IInfoPathControl](https://msdn.microsoft.com/library/bb264625.aspx)
    
- [IInfoPathControlSite](https://msdn.microsoft.com/library/bb264627.aspx)
    
## <a name="add-an-activex-control-to-the-infopath-design-environment"></a>Adicionar um controle ActiveX para o ambiente de Design do InfoPath

O comando**adicionar ou remover controles personalizados** no **painel de tarefas** controles permite que você use o **Assistente para adicionar controle personalizado** para adicionar um controle personalizado. Usando o assistente, você pode selecionar um controle ActiveX que já foi registrado ou localizar mais controles personalizados no Marketplace do Office. Depois de selecionar um controle, você pode especificar os itens a seguir. 
  
- Especifique um gabinete para instalar o controle ActiveX com seu modelo de formulário.
    
- Especifica uma propriedade de associação para associar ao XML.
    
- Especifique uma propriedade usada para ativar ou desativar o controle em resposta às regras ou assinaturas digitais, que podem ser úteis, por exemplo, quando não houver XML ou quando a formatação condicional é usada.
    
- Para especificar dados digite encadernação.
    
> [!NOTE]
> Se você estiver desenvolvendo um controle ActiveX e adicioná-lo para o **painel de tarefas** controles no InfoPath, não será possível recriar o controle ActiveX até InfoPath é fechado. 
  
## <a name="deploy-an-activex-control"></a>Implantar um controle ActiveX

Para distribuir um controle ActiveX, você pode gravar uma instalação que instala o controle no computador de destino e copia o arquivo de modelo de controle do InfoPath (TIC) e o arquivo de gabinete para a pasta do usuário, \Users\\< nome de usuário\>\AppData\ Local\Microsoft\InfoPath\Controls. Observe que, se dois ou mais desenvolvedores de duas ou estiverem colaborando no desenvolvimento de formulários com controles ActiveX, cada desenvolvedor deve ter os controles que foram adicionados para o ambiente de design InfoPath ou não será possível modificar as propriedades dos controles de InfoPath.
  
## <a name="see-also"></a>Confira também

Laboratório 6: Adicionar controles ActiveX no InfoPath 2003
  
[Criar um controle de personalizado InfoPath utilizando c# e .NET (Blog da equipe InfoPath)](https://blogs.msdn.microsoft.com/infopath/2005/04/15/creating-an-infopath-custom-control-using-c-and-net/)

