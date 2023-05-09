# minecraft-pig
A animation of a minecraft pig blinking.
import simplegui
count=0
def draw_handler(canvas):
    
    global count
    global colors
   
    
    if count==10:
        colors[2][0]="#FDB3B3"
        colors[2][1]="#FDB3B3"
        colors[2][2]="#FDB3B3"
        colors[2][4]="#FDB3B3"
        colors[2][5]="#FDB3B3"
        colors[2][6]="#FDB3B3"
    
    if count==30:
        colors[3][0]="#FDB3B3"
        colors[3][1]="#FDB3B3"
        colors[3][2]="#FDB3B3"
        colors[3][4]="#FDB3B3"
        colors[3][5]="#FDB3B3"
        colors[3][6]="#FDB3B3"
        
    if count == 75:
        colors[2][0] = "#000000"
        colors[2][1] ="#FFFFFF"
        colors[2][2] = "#FFFFFF"
        colors[2][4] ="#FFFFFF" 
        colors[2][5] ="#FFFFFF"
        colors[2][6] = "#000000"
        
    if count == 80:
        colors[3][0] = "#000000"
        colors[3][1] ="#FFFFFF"
        colors[3][2] = "#FFFFFF"
        colors[3][4] ="#FFFFFF" 
        colors[3][5] ="#FFFFFF"
        colors[3][6] = "#000000"
        
   
    

    
    
    
    
    
    
    
    
    
    

    row = 0
    col = 0
    for r in range(1, 350, 50):
        for c in range(1, 350, 50):
            canvas.draw_polygon([(c, r), (c + 50, r), (c + 50, r + 50), (c, r + 50)], 1, "black", colors[row][col])   
            col = col + 1
        row = row + 1
        col = 0
    count+=5
#********** MAIN **********

frame = simplegui.create_frame('Pic', 350, 350)
frame.set_draw_handler(draw_handler)
frame.start()
colors = [] 
colors.append(["#F8ACDA", "#F99BD4 ", "#F8ACDA", "#F8ACDA", "#F8ACDA", "#F8ACDA", "#F8ACDA"]) 
colors.append(["#F8ACDA", "#F99BD4", "#F8ACDA", "#F8ACDA", "#F8ACDA", "#F8ACDA", "#F8ACDA"]) 
colors.append(["#000000  ", "#FFFFFF", "#FFFFFF", "#F8ACDA", "#FFFFFF", "#FFFFFF", "#000000"]) 
colors.append(["#000000 ", "#FFFFFF ", "#FFFFFF", "#F99BD4", "#FFFFFF", "#FFFFFF", "#000000"]) 
colors.append(["#FDC0E5 ", "#F99BD4 ", "#F8ACDA", "#F99BD4", "#F99BD4", "#F8ACDA", "#F99BD4"]) 
colors.append(["#FDC0E5 ", "#E8BABA", "#E8BABA", "#E8BABA", "#E8BABA", "#E8BABA", "#F99BD4"]) 
colors.append(["#FDC0E5 ", "#C59F9F", "#E8BABA", "#EACCCC", "#EACCCC", "#C59F9F", "#F99BD4"]) 
