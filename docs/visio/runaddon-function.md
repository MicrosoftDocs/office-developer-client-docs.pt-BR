---
title: Função RUNADDON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251492
localization_priority: Normal
ms.assetid: 122c1d30-3cb9-7e7d-b4cc-e93ab8e4da4f
description: Executa um complemento ou uma macro em um projeto do Microsoft Visual Basic for Applications (VBA).
ms.openlocfilehash: 280f6eaf1e5db045d8c1d22965df00960d188112
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432006"
---
# <a name="runaddon-function"></a>Função RUNADDON

Executa um complemento ou uma macro em um projeto do Microsoft Visual Basic for Applications (VBA). 
  
## <a name="syntax"></a>Sintaxe

RUNADDON (" *cadeia de caracteres* ") 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _string_ <br/> |Obrigatório  <br/> |**Cadeia de caracteres** <br/> | O nome de um complemento na coleção **Addons** ou de uma macro em um projeto VBA.  <br/> |
   
## <a name="remarks"></a>Comentários

Se o projeto do documento que contém a chamada de função RUNADDON (ou outro projeto se for referenciado) não tiver uma macro (um procedimento sem argumentos) chamado _String_, o Microsoft Visio executará o complemento chamado _String_. Se nenhuma _cadeia de caracteres_ nomeada de complemento puder ser encontrada, o Visio não fará nada e não informará nenhum erro. (Você pode usar a propriedade **TraceFlags** para monitorar os procedimentos e complementos que o Visio tenta executar.) 
  
Ao chamar um procedimento em um módulo padrão, é recomendável prefixar a cadeia de caracteres com o nome do módulo que contém o procedimento (por exemplo, *ModuleName. ProcName*), porque mais de um módulo pode ter um procedimento com o mesmo nome. 
  
Para chamar um procedimento em um projeto diferente do projeto do documento que contém a chamada de função RUNADDON, use a sintaxe *ProjName. modName. ProcName* (você deve ter definido explicitamente uma referência ao *ProjName* no projeto VBA). 
  
> [!NOTE]
>  Iniciando com o Visio 2002, a função RUNADDON não pode executar uma sequência de caracteres contendo código VBA arbitrário. Códigos que tenham anteriormente passado para a função RUNADDON podem ser movidos para um procedimento no projeto VBA de um documento que é chamado a partir da função RUNADDON. 
  
Para obter mais informações sobre a execução de códigos no Visio, consulte [Sobre configurações de segurança e execução de códigos no Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) nesta Referência da ShapeSheet. 
  
Em versões anteriores do Visio, essa função aparece como _RUNADDON. As versões 4.0 e posteriores do Visio aceitam os dois estilos. 
  
## <a name="example-1"></a>Exemplo 1

RUNADDON ("Calendar. exe")
  
Inicia um complemento chamado Calendar. exe.
  
## <a name="example-2"></a>Exemplo 2

RUNADDON("Arranjar Formas")
  
Inicia o complemento (implementado em VSL) cujo nome é Arranjar formas.
  
## <a name="example-3"></a>Exemplo 3

RUNADDON ("ThisDocument. ReportStatistics")
  
Chama a macro ReportStatistics no módulo **EsteDocumento** no projeto do documento contendo essa chamada de função. 
  
> [!NOTE]
>  Para invocar a macro no módulo **ThisDocument**, anteceda a cadeia de caracteres com "EsteDocumento" como mostrado. 
  
## <a name="example-4"></a>Exemplo 4

RUNADDON (" *ModuleName* . ReportStatistics ") 
  
Chama a macro ReportStatistics em *ModuleName* no projeto de documento que contém essa chamada de função. 
  

