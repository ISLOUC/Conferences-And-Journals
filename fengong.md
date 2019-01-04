<table id=tbTabs cellpadding=0 cellspacing=0>";

 var iCellCount=(c_lTabs+1)*2;

 var i;
 for (i=0;i<iCellCount;i+=2)
  szHTML+="<col width=1><col>";

 var iRow;
 for (iRow=0;iRow<6;iRow++) {

  szHTML+="<tr>";

  if (iRow==5)
   szHTML+="<td colspan="+iCellCount+"></td>";
  else {
   if (iRow==0) {
    for(i=0;i<iCellCount;i++)
     szHTML+="<td height=1 class=\"clBorder\"></td>";
   } else if (iRow==1) {
    for(i=0;i<c_lTabs;i++) {
     szHTML+="<td height=1 nowrap class=\"clBorder\">&nbsp;</td>";
     szHTML+=
      "<td id=tdTab height=1 nowrap class=\"clTab\" onmouseover=\"parent.fnMouseOverTab("+i+");\" onmouseout=\"parent.fnMouseOutTab("+i+");\">"+
      "<a href=\""+document.all.item("shLink")[i].href+"\" target=\"frSheet\" id=aTab>&nbsp;"+c_rgszSh[i]+"&nbsp;</a></td>";
    }
    szHTML+="<td id=tdTab height=1 nowrap class=\"clBorder\"><a id=aTab>&nbsp;</a></td><td width=100%></td>";
   } else if (iRow==2) {
    for (i=0;i<c_lTabs;i++)
     szHTML+="<td height=1></td><td height=1 class=\"clBorder\"></td>";
    szHTML+="<td height=1></td><td height=1></td>";
   } else if (iRow==3) {
    for (i=0;i<iCellCount;i++)
     szHTML+="<td height=1></td>";
   } else if (iRow==4) {
    for (i=0;i<c_lTabs;i++)
     szHTML+="<td height=1 width=1></td><td height=1></td>";
    szHTML+="<td height=1 width=1></td><td></td>";
   }
  }
  szHTML+="</tr>";
 }

 szHTML+="</table>
