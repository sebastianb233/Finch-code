public class FinchTest1 {
    private Finch finch;

    public FinchTest1() {
        finch = new Finch(); // Initiate Finch robot
    }

    public void FinchButtonScore() {
        int s = 0; // Score variable

        while (true) { // Keeps program running
            if (finch.getButton("A") || finch.getButton("B")) { 
                s++;  // Increment score
                System.out.println("Score: " + s); 

                while (finch.getButton("A") || finch.getButton("B")) { 
                    try {
                        Thread.sleep(50);
                    } catch (InterruptedException e) {
                        e.printStackTrace();
                    }
                }
            }
        }
    }

    public boolean detectTape() {
        int tapeThreshold = 50; // Tape reflectivity threshold
        int leftLight = finch.getLight("L");
        int rightLight = finch.getLight("R");

        System.out.println("Left Light: " + leftLight + ", Right Light: " + rightLight);
        return leftLight >= tapeThreshold || rightLight >= tapeThreshold;
        
    }
    

    public void times(int time) {
        // Ensure valid time range
        time = Math.min(135, Math.max(32, time));

        for (int i = 0; i < time; i++) {
            for (int j = 0; j < 5; j++) {
                numbers(j);
                finch.pause(time);
            }
        }
    }

    public void numbers(int num) {
        int[] display = new int[25];

        switch (num) {
            case 1: display = new int[]{0,0,1,0,0,0,1,1,0,0,1,0,1,0,0,0,0,1,0,0,1,1,1,1,1}; break;
            case 2: display = new int[]{0,1,1,1,0,1,0,0,1,0,0,0,1,0,0,0,1,0,0,0,1,1,1,1,1}; break;
            case 3: display = new int[]{0,1,1,1,0,1,0,0,0,1,0,0,1,1,0,1,0,0,0,1,0,1,1,1,0}; break;
            case 4: display = new int[]{1,0,1,0,0,1,0,1,0,0,1,1,1,1,1,0,0,1,0,0,0,0,1,0,0}; break;
        }

        for (int i = 0; i < display.length; i++) {
            display[i] = display[i] == 0 ? 32 : 135;
        }

        finch.setDisplay(display);
    }

    public static void main(String[] args) {
        FinchTest1 test = new FinchTest1();
        test.FinchButtonScore();
    }
    
}
