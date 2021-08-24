// Sandipan Mondal


import java.awt.Color;

public class ArtCollage {

    // The orginal picture
    private Picture original;

    // The collage picture
    private Picture collage;

    // The collage Picture consists of collageDimension X collageDimension tiles
    private int collageDimension;

    // A tile consists of tileDimension X tileDimension pixels
    private int tileDimension;
    
    /*
     * One-argument Constructor
     * 1. set default values of collageDimension to 4 and tileDimension to 100
     * 2. initializes original with the filename image
     * 3. initializes collage as a Picture of tileDimension*collageDimension x tileDimension*collageDimension, 
     *    where each pixel is black (see all constructors for the Picture class).
     * 4. update collage to be a scaled version of original (see scaling filter on Week 9 slides)
     *
     * @param filename the image filename
     */
    public ArtCollage (String filename) {

        this.collageDimension=4;
        this.tileDimension=100;
        this.original=new Picture(filename);
        this.collage=new Picture(tileDimension*collageDimension,tileDimension*collageDimension);
        
        Picture originalV2 = new Picture(tileDimension*collageDimension,tileDimension*collageDimension);
        for(int x =0; x < tileDimension*collageDimension; x++)
            for(int y = 0; y <tileDimension*collageDimension; y++)
            {
                Color wow= original.get(x*original.width()/(tileDimension*collageDimension), y*original.height()/(tileDimension*collageDimension));
                originalV2.set(x,y,wow);
            }
            collage=originalV2;
        
    }

    /*
     * Three-arguments Constructor
     * 1. set default values of collageDimension to cd and tileDimension to td
     * 2. initializes original with the filename image
     * 3. initializes collage as a Picture of tileDimension*collageDimension x tileDimension*collageDimension, 
     *    where each pixel is black (see all constructors for the Picture class).
     * 4. update collage to be a scaled version of original (see scaling filter on Week 9 slides)
     *
     * @param filename the image filename
     */
    public ArtCollage (String filename, int td, int cd) {

       this.collageDimension=cd;
       this.tileDimension=td;
       this.original= new Picture(filename);
       this.collage=new Picture(td*cd,td*cd); //DIDN'T FINISH NUMBER 4
       
       Picture originalV2 = new Picture(tileDimension*collageDimension,tileDimension*collageDimension);
       for(int x =0; x < tileDimension*collageDimension; x++)
           for(int y = 0; y <tileDimension*collageDimension; y++)
           {
               Color wow= original.get(x*original.width()/(tileDimension*collageDimension), y*original.height()/(tileDimension*collageDimension));
               originalV2.set(x,y,wow);
           }
           collage=originalV2;

    }

    /*
     * Returns the collageDimension instance variable
     *
     * @return collageDimension
     */
    public int getCollageDimension() {

	    return collageDimension;
    }

    /*
     * Returns the tileDimension instance variable
     *
     * @return tileDimension
     */
    public int getTileDimension() {

	    return tileDimension;
    }

    /*
     * Returns original instance variable
     *
     * @return original
     */
    public Picture getOriginalPicture() {

	    return original;
    }

    /*
     * Returns collage instance variable
     *
     * @return collage
     */
    public Picture getCollagePicture() {

	    return collage;
    }
    
    /*
     * Display the original image
     * Assumes that original has been initialized
     */
    public void showOriginalPicture() {

	    original.show();
    }

    /*
     * Display the collage image
     * Assumes that collage has been initialized
     */
    public void showCollagePicture() {

	    collage.show();
    }

    /*
     * Replaces the tile at collageCol,collageRow with the image from filename
     * Tile (0,0) is the upper leftmost tile
     *
     * @param filename image to replace tile
     * @param collageCol tile column
     * @param collageRow tile row
     */
    public void replaceTile (String filename,  int collageCol, int collageRow) {
        Picture pic = new Picture(filename);
        Picture originalV2 = new Picture(tileDimension*collageDimension,tileDimension*collageDimension);
       for(int x =0; x < tileDimension; x++)
           for(int y = 0; y <tileDimension; y++)
           {
               Color wow= pic.get(x*pic.width()/(tileDimension), y*pic.height()/(tileDimension));
               originalV2.set(x,y,wow);
           }
        for(int x = 0; x<tileDimension; x++)
        for(int y = 0; y<tileDimension; y++)
        {
            collage.set(((collageCol)*tileDimension)+x,((collageRow)*tileDimension)+y,originalV2.get(x,y));
        }
    }
    
    /*
     * Makes a collage of tiles from original Picture
     * original will have collageDimension x collageDimension tiles, each tile
     * has tileDimension X tileDimension pixels
     */
    public void makeCollage () {
       
        Picture originalV2 = new Picture(tileDimension*collageDimension,tileDimension*collageDimension);
       for(int x =0; x < tileDimension; x++)
           for(int y = 0; y <tileDimension; y++)
           {
               Color wow= original.get(x*original.width()/(tileDimension), y*original.height()/(tileDimension));
               originalV2.set(x,y,wow);
           }
for(int a = 0; a<collageDimension; a++)  
    for(int b = 0; b<collageDimension; b++) 
        for(int x = 0; x<tileDimension; x++)
            for(int y = 0; y<tileDimension; y++)
            {
                collage.set((a*tileDimension)+x,(b*tileDimension)+y,originalV2.get(x,y));
            }
        
        /* IDEA: match each pixel one by one usign a nested for loop. Now that will create 1 tile. But you need to create a collage of tiles
        So, you have to put that entire nested for loop into another nested for loop to make collage. Use color get and void set (int col...)*/
       
    }

    /*
     * Colorizes the tile at (collageCol, collageRow) with component 
     * 
     * @param component is either red, blue or green
     * @param collageCol tile column
     * @param collageRow tile row
     */
    public void colorizeTile (String component,  int collageCol, int collageRow) {

        
    for(int x = 0; x<tileDimension; x++)
    {
        for(int y = 0; y<tileDimension; y++)
        {
            Color store = collage.get(((collageCol)*tileDimension)+x, ((collageRow)*tileDimension)+y);
            if(component.equals("red"))
                collage.set(((collageCol)*tileDimension)+x,((collageRow)*tileDimension)+y,new Color(store.getRed(),0,0));
            if(component.equals("blue"))
                collage.set(((collageCol)*tileDimension)+x,((collageRow)*tileDimension)+y,new Color(0,0,store.getBlue()));
            if(component.equals("green"))
                collage.set(((collageCol)*tileDimension)+x,((collageRow)*tileDimension)+y,new Color(0,store.getGreen(),0));
           
        }
    }
}


 
    /*
     * Grayscale tile at (collageCol, collageRow)
     * (see CS111 Week 9 slides, the code for luminance is at the book's website)
     *
     * @param collageCol tile column
     * @param collageRow tile row
     */

    public void grayscaleTile (int collageCol, int collageRow) {

        for(int x = 0; x < tileDimension; x++)
            for(int y = 0; y < tileDimension; y++)
            {
                collage.set(((collageCol)*tileDimension)+x,((collageRow)*tileDimension)+y, Luminance.toGray(collage.get(((collageCol)*tileDimension)+x,((collageRow)*tileDimension)+y)));
            }
    }


    /*
     *
     *  Test client: use the examples given on the assignment description to test your ArtCollage
     */
    public static void main (String[] args) {

        ArtCollage art = new ArtCollage("Ariel.jpg",200,4); 
        art.showCollagePicture();
        art.makeCollage();
        art.replaceTile("baloo.jpeg", 3, 2);
        art.colorizeTile("green", 3, 2);
        art.showCollagePicture();
        
    }
}
