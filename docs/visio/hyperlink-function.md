---
title: Função HYPERLINK
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251441
localization_priority: Normal
ms.assetid: 943636a6-e135-a626-7924-11e238156548
description: Navega para o endereço especificado, que pode ser um arquivo, UNC ou URL caminho.
ms.openlocfilehash: 4e86fd3682d5d9e26c52839e76d2016d654b3141
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19772032"
---
# <a name="hyperlink-function"></a>Função HYPERLINK

Navega para o endereço especificado, que pode ser um arquivo, UNC ou URL caminho.
  
## <a name="syntax"></a>Sintaxe

HYPERLINK ("* * *endereço* * *" [,"* * *subaddress* * *","* * *extrainfo* * *", * * *janela* * *, "* * *quadro* * *"]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _endereço_ <br/> |Obrigatório  <br/> |**String** <br/> |Um caminho completo ou relativo.  <br/> |
| _Subendereço_ <br/> |Opcional  <br/> |**String** <br/> |Especifica uma localidade no endereço deseja estabelecer um vínculo. Por exemplo, se o endereço for um arquivo do Microsoft Visio, subendereço pode ser um nome de página; Se um arquivo do Microsoft Excel, o subendereço pode ser uma planilha ou um intervalo em uma planilha; Se uma URL para uma página HTML, o subendereço pode ser uma âncora.  <br/> |
| _ExtraInfo_ <br/> |Opcional  <br/> |**String** <br/> |Passa as informações utilizadas para resolver o URL, como as coordenadas de um mapa de imagens.  <br/> |
| _janela_ <br/> |Opcional  <br/> |**Boolean** <br/> |Especifica se o hiperlink será aberto em uma nova janela. O valor padrão é FALSO.  <br/> |
| _quadro_ <br/> |Opcional  <br/> |**String** <br/> | Especifica o nome de uma moldura para servir de destino quando o Visio for aberto como um documento ativo em um navegador ActiveX, como o Microsoft Internet Explorer 3.0 ou superior. O padrão é uma cadeia de caracteres vazia.  <br/> |
   
## <a name="remarks"></a>Comentários

Se o documento não tiver caminho de base, o Visio navegará de acordo com o caminho do documento. Se o documento não tiver sido salvo, o hiperlink não será definido. 
  
Caminhos relativos baseiam-se no campo **base do hiperlink** especificado na caixa de diálogo **Propriedades do Visio** . 
  
Utilize a função GOTOPAGE para navegar em páginas de um documento. 
  
## <a name="example-1"></a>Exemplo 1

 `HYPERLINK("C:\My Documents\Drawing1.vsdx")`
  
## <a name="example-2"></a>Exemplo 2

 `HYPERLINK("\\Server\Share\Drawing1.vsdx")`
  
## <a name="example-3"></a>Exemplo 3

 `HYPERLINK("http://www.microsoft.com")`
  
## <a name="example-4"></a>Exemplo 4

 `HYPERLINK("..\data.xlsx","sheet1!A1")`
  

