 function YONEX()
end
function setvalue(address,flags,value) YONEX('Modify address value(Address, value type, value to be modified)') local tt={} tt[1]={} tt[1].address=address tt[1].flags=flags tt[1].value=value gg.setValues(tt) end

gg.alert("┏⊳ ᴛᴇʟᴇɢʀᴀᴍ @YONEXGAMING\n┣⊳ ᴛʜᴀɴᴋs ғᴏʀ sᴜᴘᴘᴏʀᴛ\n┗⊳ sᴄʀɪᴘᴛ ᴡᴏʀᴋ ᴡɪᴛʜᴏᴜᴛ ʙʏᴘᴀss\n\n● PRIVATE SCRIPT BY YONEX GAMING")
function Main()
  GAMAT = gg.multiChoice({
    "╔✧[ʟᴏʙʙʏ] \n╚✧ʟᴇss ʀᴇᴄᴏɪʟ",
    "╔✧[ʟᴏʙʙʏ] \n╚✧BYPASS",
    "╔✧[ʟᴏʙʙʏ] \n╚✧ᴀɪᴍʙᴏᴛ",
    "╔✧[ʟᴏʙʙʏ] \n╚✧ᴡɪᴅᴇ ᴠɪᴇᴡ",
    "╔✧[ʟᴏʙʙʏ] \n╚✧ʙʟᴀᴄᴋ ᴄᴏʟᴏʀ",  
    "╔✧[ʟᴏʙʙʏ] \n╚✧ʙʟᴀᴄᴋ sᴋʏ",  
    "╔✧[ʟᴏʙʙʏ] \n╚✧ᴅᴀʀᴋ ᴍᴀᴘ",   
    "╔✧[ʟᴏʙʙʏ] \n╚✧ғᴏɢ ʀᴇᴍᴏᴠᴇ",    
    "╔✧[ʟᴏʙʙʏ] \n╚✧ɢʀᴀss ʀᴇᴍᴏᴠᴇ",     
    "[ᴄʜᴀɴɴᴇʟ ʟɪɴᴋ ᴄᴏᴘʏ]",
    "╔✧\n╚☩🅴🆇🅸🆃"
  }, nil, (os.date("VERSION=2.0\n┏⊳ @YONEXGAMING\n┣⊳ @YONEX+@MRYONEX\n┣⊳ @YX\n┗⊳%A, %d %B %Y %H:%M%p ")))
  if GAMAT == nil then
  else
    if GAMAT[1] == true then
      L()
    end
    if GAMAT[2] == true then
      C()
    end
    if GAMAT[3] == true then
      A()
    end
    if GAMAT[4] == true then
      W()
    end
     if GAMAT[5] == true then
      BCLR()
    end   
     if GAMAT[6] == true then
      BS()
    end    
     if GAMAT[7] == true then
      BM()
    end          
     if GAMAT[8] == true then
      FR()
    end        
     if GAMAT[9] == true then
      GR()
    end            
   if GAMAT[10] == true then
      CP()
    end     
    if GAMAT[11] == true then
      Exit()
    end
  end
  XGCK = -1
end
function CP()
gg.alert("💝ᴄᴏᴘʏ ᴅᴏɴᴇ  💝")
gg.copyText("https://t.me/yonexgaming")
end
function L()
so=gg.getRangesList('libUE4.so')[1].start
py=0x1227C24
setvalue(so+py,16,0)
gg.toast("https://t.me/YONEXGAMING")
end
function C()
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("2.2958874e-41;16384D;16384D;16384D;16384D;16384D::24", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
if gg.getResultCount() == 0 then
else
gg.searchNumber("2.2958874e-41", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
n = gg.getResultCount()
jz = gg.getResults(n)
for i = 1, n do
gg.addListItems({[1] = {address = jz[i].address - 252,flags = 4,freeze = true,value = 70086}})
gg.addListItems({[1] = {address = jz[i].address - 236,flags = 4,freeze = true,value = 70086}})
gg.addListItems({[1] = {address = jz[i].address - 232,flags = 4,freeze = true,value = 70086}})
gg.addListItems({[1] = {address = jz[i].address - 72,flags = 4,freeze = true,value = 70086}})
gg.addListItems({[1] = {address = jz[i].address - 68,flags = 4,freeze = true,value = 70086}})
gg.addListItems({[1] = {address = jz[i].address - 64,flags = 4,freeze = true,value = 70086}})
gg.addListItems({[1] = {address = jz[i].address + 30,flags = 4,freeze = true,value = 119}})
gg.addListItems({[1] = {address = jz[i].address + 130,flags = 4,freeze = true,value = 70086}})
gg.addListItems({[1] = {address = jz[i].address + 180,flags = 4,freeze = true,value = 70086}})
gg.addListItems({[1] = {address = jz[i].address + 200,flags = 4,freeze = true,value = 4451}})
gg.addListItems({[1] = {address = jz[i].address + 300,flags = 4,freeze = true,value = 0}})
gg.addListItems({[1] = {address = jz[i].address + 310,flags = 4,freeze = true,value = 70086}})
gg.addListItems({[1] = {address = jz[i].address + 360,flags = 4,freeze = true,value = 70086}})
gg.addListItems({[1] = {address = jz[i].address + 450,flags = 4,freeze = true,value = 70086}})
gg.addListItems({[1] = {address = jz[i].address + 650,flags = 4,freeze = true,value = 70086}})
gg.addListItems({[1] = {address = jz[i].address + 800,flags = 4,freeze = true,value = 70086}})
gg.clearList()
end
end
gg.clearResults()
gg.setVisible(false)
gg.setRanges(gg.REGION_C_ALLOC)
gg.setVisible(false)
gg.searchNumber("32804;98386", gg.TYPE_DWORD)
gg.refineNumber("32804", gg.TYPE_DWORD)
gg.getResults(99999)
gg.setVisible(false)
gg.editAll("0", gg.TYPE_DWORD)
gg.setVisible(false)
gg.clearResults()
gg.clearResults()
gg.clearResults()
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.setVisible(false)
gg.searchNumber("25536;34817", gg.TYPE_DWORD)
gg.refineNumber("25536", gg.TYPE_DWORD)
gg.getResults(99999)
gg.setVisible(false)
gg.editAll("0", gg.TYPE_DWORD)
gg.setVisible(false)
gg.clearResults()
gg.clearResults()
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.setVisible(false)
gg.searchNumber("32768;98288", gg.TYPE_DWORD)
gg.refineNumber("32768", gg.TYPE_DWORD)
gg.getResults(99999)
gg.setVisible(false)
gg.editAll("0", gg.TYPE_DWORD)
gg.setVisible(false)
gg.clearResults()
gg.clearResults()
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.setVisible(false)
gg.searchNumber("135682;144387", gg.TYPE_DWORD)
gg.refineNumber("135682", gg.TYPE_DWORD)
gg.getResults(50000)
gg.setVisible(false)
gg.editAll("0", gg.TYPE_DWORD)
gg.setVisible(false)
gg.clearResults()
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.setVisible(false)
gg.searchNumber("134658;131586", gg.TYPE_DWORD)
gg.refineNumber("134658", gg.TYPE_DWORD)
gg.getResults(50000)
gg.setVisible(false)
gg.editAll("0", gg.TYPE_DWORD)
gg.setVisible(false)
gg.clearResults()
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.setVisible(false)
gg.searchNumber("4096;135682", gg.TYPE_DWORD)
gg.refineNumber("4096", gg.TYPE_DWORD)
gg.getResults(50000)
gg.setVisible(false)
gg.editAll("0", gg.TYPE_DWORD)
gg.setVisible(false)
gg.clearResults()
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("157567", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("0", gg.TYPE_DWORD)
gg.clearResults()
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("135938", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("0", gg.TYPE_DWORD)
gg.clearResults()
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("135170", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("0", gg.TYPE_DWORD)
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("135426", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("0", gg.TYPE_DWORD)
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("135212", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("0", gg.TYPE_DWORD)
gg.clearResults()
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.setVisible(false)
gg.searchNumber("134914;262403", gg.TYPE_DWORD)
gg.refineNumber("134914", gg.TYPE_DWORD)
gg.getResults(50000)
gg.setVisible(false)
gg.editAll("0", gg.TYPE_DWORD)
gg.setVisible(false)
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.setVisible(false)
gg.searchNumber("133378;262403", gg.TYPE_DWORD)
gg.refineNumber("133378", gg.TYPE_DWORD)
gg.getResults(50000)
gg.setVisible(false)
gg.editAll("0", gg.TYPE_DWORD)
gg.setVisible(false)
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.setVisible(false)
gg.searchNumber("131330;133634", gg.TYPE_DWORD)
gg.refineNumber("131330", gg.TYPE_DWORD)
gg.getResults(50000)
gg.setVisible(false)
gg.editAll("0", gg.TYPE_DWORD)
gg.setVisible(false)
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.setVisible(false)
gg.searchNumber("131842;132098", gg.TYPE_DWORD)
gg.refineNumber("131842", gg.TYPE_DWORD)
gg.getResults(50000)
gg.setVisible(false)
gg.editAll("0", gg.TYPE_DWORD)
gg.setVisible(false)
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("133634", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("0", gg.TYPE_DWORD)
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("131331", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("0", gg.TYPE_DWORD)
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("132098", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("0", gg.TYPE_DWORD)
gg.clearResults()
end
function A()
so=gg.getRangesList('libUE4.so')[1].start
py=0x22BF3B0
setvalue(so+py,16,0)
gg.toast("https://t.me/YONEXGAMING")
end
function W()
so=gg.getRangesList('libUE4.so')[1].start
py=0x34D7E30
setvalue(so+py,16,265)
gg.toast("https://t.me/YONEXGAMING")
end
function BCLR()
so=gg.getRangesList('libUE4.so')[1].start
py=0x2ACCC28
setvalue(so+py,16,1090519040)
gg.toast("https://t.me/YONEXGAMING")
end

function BS()
so=gg.getRangesList('libUE4.so')[1].start
py=0x37869D0
setvalue(so+py,4,-1222130000)
gg.toast("https://t.me/YONEXGAMING")
end
function BM()
so=gg.getRangesList('libUE4.so')[1].start
py=0x2BC4924
setvalue(so+py,4,550292)
gg.toast("https://t.me/YONEXGAMING")
end

function FR()
so=gg.getRangesList('libUE4.so')[1].start
py=0x2A43A18
setvalue(so+py,4,0)
gg.toast("https://t.me/YONEXGAMING")
end
function GR()
so=gg.getRangesList('libUE4.so')[1].start
py=0x228D948
setvalue(so+py,4,0)
gg.toast("https://t.me/YONEXGAMING")
end

function Exit()
  print("📍@YONEX📍")
  print("ᴛᴇʟᴇɢʀᴀᴍ ᴄʜᴀɴɴᴇʟ : @YONEXGAMING ")
  gg.skipRestoreState()
  os.exit()
end


while true do
  if gg.isVisible(true) then
    XGCK = 1
    gg.setVisible(false)
  end
  gg.clearResults()
  if XGCK == 1 then
    Main()
  end
end

